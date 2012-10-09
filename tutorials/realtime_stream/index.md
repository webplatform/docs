{{Page_Title|Real-time updates in stream congress}}
{{Flags
|High-level issues=Needs Flags
}}
{{Byline
|Name=Luigi Montanez
|URL=http://www.html5rocks.com/profiles/#luigimontanez
|Published=March 17, 2011
}}
{{Summary_Section|How to build web apps that communicate in real time with a server.}}
{{Tutorial
|Content=Through [http://www.html5rocks.com/tutorials/websockets/basics/ WebSockets] and [http://www.html5rocks.com/tutorials/eventsource/basics/ EventSource], HTML5 enables developers to build web apps that communicate in real time with a server. [http://streamcongress.com Stream Congress] (available in the [https://chrome.google.com/webstore/detail/ahebmhmbjonbglfkghfennmigkcmpbjp Chrome Web Store]) provides live updates about the workings of the United States Congress. It streams floor updates from both the House and Senate, relevant news updates, tweets from members of Congress, and other social media updates. The app is meant to be left open all day as it captures the business of Congress.

==Starting with WebSockets==

The WebSockets spec has gotten quite a bit of attention for what it enables: a stable, bi-directional [http://www.csc.villanova.edu/~mdamian/Sockets/TcpSockets.htm TCP socket] between the browser and server. There is no data format imposed on the TCP socket; the developer is free to define a messaging protocol. In practice, passing JSON objects around as strings is most convenient. The client-side JavaScript code to listen for live updates is clean and simple:
 
<syntaxhighlight lang="JavaScript">
 var liveSocket = new WebSocket("ws://streamcongress.com:8080/live");
 liveSocket.onmessage = function(payload) {
   addToStream(JSON.parse(payload.data).reverse());
 };
</syntaxhighlight>

While browser support for WebSockets is straightforward, server-side support is still in the formative stage. [http://socket.io/ Socket.IO] on Node.js provides one of the most mature and robust server-side solutions. An event-driven server like Node.js is the right fit for WebSockets. For alternative implementations, Python developers can use [http://twistedmatrix.com/trac/ Twisted] and [http://www.tornadoweb.org/ Tornado], while Ruby developers have [http://rubyeventmachine.com/ EventMachine].

===Introducing Cramp===

[https://github.com/lifo/cramp Cramp] is an asynchronous Ruby web framework that runs on top of EventMachine. It’s written by [http://m.onkey.org/ Pratik Naik], a member of the Ruby on Rails core team. Providing a simple domain specific language (DSL) for real-time web apps, Cramp is an ideal choice for Ruby web developers. Those familiar with writing controllers in Ruby on Rails will recognize Cramp's style:
 
<syntaxhighlight lang="yaml">
 require "rubygems"
 require "bundler"
 Bundler.require
 require 'cramp'
 require 'http_router'
 require 'active_support/json'
 require 'thin'
 
 Cramp::Websocket.backend = :thin
 
 class LiveSocket < Cramp::Websocket
    periodic_timer :check_activities, :every => 15
 
    def check_activities
      @latest_activity {{!}}{{!}}= nil
      new_activities = find_activities_since(@latest_activity)
      @latest_activity = new_activities.first unless new_activities.empty?
      render new_activities.to_json
    end
  end
 
 routes = HttpRouter.new do
   add('/live').to(LiveSocket)
 end
 run routes
</syntaxhighlight>

Because Cramp sits on top of the non-blocking EventMachine, there are several considerations to keep in mind:

* Non-blocking database drivers must be used, like [https://github.com/oldmoe/mysqlplus MySQLPlus] and [https://github.com/bcg/em-mongo em-mongo].
* Event-driven web servers must be used. Support is built in for [http://code.macournoyer.com/thin/ Thin] and [http://rainbows.rubyforge.org/ Rainbows].
* The Cramp app must be run separately from the main Rails app that powers Stream Congress, restarted and monitored independently.

===Current Limitations===

WebSockets suffered a setback on December 8, 2010 when a security vulnerability was publicized. Both [http://hacks.mozilla.org/2010/12/websockets-disabled-in-firefox-4/ Firefox and Opera] removed browser support for WebSockets. While no pure JavaScript polyfill exists, there is a [https://github.com/gimite/web-socket-js/ Flash fallback] that has been widely adopted. However, relying on Flash is far from ideal. Even though Chrome and Safari continue to support WebSockets, it became clear that to support all modern browsers without relying on Flash, WebSockets would need to be replaced.

==Rolling back to AJAX polling==

The decision was made to move away from WebSockets and back to “old-school” AJAX polling. While much less efficient from a disk and network I/O perspective, AJAX polling simplified the technical implementation of Stream Congress. Most significantly, the need for a separate Cramp app was eliminated. The AJAX endpoint was instead provided by the Rails app. The client-side code was modified to support jQuery AJAX polling:
 
<syntaxhighlight>
 var fillStream = function(mostRecentActivity) {
   $.getJSON(requestURL, function(data) {
     addToStream(data.reverse());
     setTimeout(function() {fillStream(recentActivities.last());}, 15000);
   });
 };
</syntaxhighlight>

AJAX polling, though, is not without its downsides. Relying on the HTTP request/response cycle means that the server sees constant load even when there aren’t any new updates. And of course, AJAX polling doesn’t take advantage of what HTML5 has to offer.

==EventSource: The right tool for the job==

Up to this point, a key factor was ignored about the nature of Stream Congress: the app only needs to stream updates one way, from server to client — downstream. It didn't need to be real-time, upstream client-to-server communication.

In this sense, WebSockets is overkill for Stream Congress. Server-to-client communication is so common that it’s been given a general term: push. In fact, many existing solutions for WebSockets, from the hosted [http://pusherapp.com PusherApp] to the Rails library [https://github.com/socky Socky], optimize for push and don’t support client-to-server communication at all.

Enter EventSource, also called Server-Sent Events. The specification compares favorably to WebSockets in the context to server to client push:

* A similar, simple JavaScript API on the browser side.
* The open connection is HTTP-based, not dropping to the low level of TCP.
* Automatic reconnection when the the connection is closed.

===Going Back to Cramp===

In recent months, Cramp has added support for EventSource. The code is very similar to the WebSockets implementation:
 
<syntaxhighlight>
 class LiveEvents < Cramp::Action
   self.transport = :sse
 
   periodic_timer :latest, :every => 15
 
   def latest
     @latest_activity &#124;&#124;= nil
     new_activities = find_activities_since(@latest_activity)
     @latest_activity = new_activities.first unless new_activities.empty?
     render new_activities.to_json
   end
 end
 
 routes = HttpRouter.new do
   add('/').to(LiveEvents)
 end
 run routes
</syntaxhighlight>

A significant issue to keep in mind with EventSource is that cross-domain connections are not allowed. This means that the Cramp app must be served from the same streamcongress.com domain as the main Rails app. This can be accomplished with proxying at the web server. Assuming the Cramp app is powered by Thin and running on port 8000, the Apache configuration looks like so:
 
<syntaxhighlight>
 LoadModule  proxy_module         /usr/lib/apache2/modules/mod_proxy.so
 LoadModule  proxy_http_module    /usr/lib/apache2/modules/mod_proxy_http.so
 LoadModule  proxy_balancer_module    /usr/lib/apache2/modules/mod_proxy_balancer.so
 
 <VirtualHost *:80>
   ServerName streamcongress.com
   DocumentRoot /projects/streamcongress/www/current/public
   RailsEnv production
   RackEnv production
   <Directory /projects/streamcongress/www/current/public>
     Order allow,deny
     Allow from all
     Options -MultiViews
   </Directory>
 
   <Proxy balancer://thin>
     BalancerMember http://localhost:8000
   </Proxy>
   ProxyPass /live balancer://thin/
   ProxyPassReverse /live balancer://thin/
   ProxyPreserveHost on
 
 </VirtualHost>
</syntaxhighlight>

This configuration sets an EventSource endpoint at <code>streamcongress.com/live</code>.

===Stable Polyfill===

One of the most significant advantages of EventSource over WebSockets is that fallback is completely JavaScript-based, with no dependence on Flash. Remy Sharp’s [https://github.com/remy/polyfills polyfill] accomplishes this by implementing long-polling in browsers that don’t support EventSource natively. Thus, EventSource works today on all modern browsers with JavaScript enabled.

==Conclusion==

HTML5 opens the door to many new and exciting web development possibilities. With WebSockets and EventSource, web developers now have clean, well-defined standards to enable real-time web apps. But not all users run modern browsers. Graceful degradation must be considered when choosing to implement these technologies. And tooling on the server side for WebSockets and EventSource is still in the early stages. It’s important to keep these factors in mind when developing real-time HTML5 apps.
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=WebSockets
|Chrome_supported=Yes
|Chrome_version=21
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=14
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=EventSource (Server-sent Events)
|Chrome_supported=Yes
|Chrome_version=21
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=14
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=WebSockets
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=4.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=EventSource (Server-sent Events)
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=4.0
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOMEvents, Webworkers}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=http://www.html5rocks.com/tutorials/casestudies/sunlight_streamcongress/
}}