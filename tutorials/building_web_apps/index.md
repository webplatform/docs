{{Page_Title}}
{{Flags}}
{{Byline}}
{{Summary_Section|In this tutorial, we'll provide you with the architectural understanding, frameworks and tools you'll need in order to create web apps.  We'll also explain how they should be used and how they fit together.}}
{{Tutorial
|Content=== Architecture ==

First, think of this simple use case. A user lands on a mobile web app that displays movie listings and clicks on a link to the "Inception" movie.

[[File:web_app_flow_1.png|center]]

This is how a traditional website would handle the user experience, using redirects.

[[File:web_app_flow_2.png|center]]

First, the user lands on the movie listing website. The web server sends back all of the markup (HTML, CSS), JavaScript and data in order to display the page. Next, the user clicks on the "Inception" movie. The browser is then redirected to <code>/movies/inception</code>. 

Again, the server sends back all of the markup, JavaScript and data in order to display the page. It can often be a jarring user experience because you cannot control the visual flow of the last content disappearing and the new content appearing. It's also likely this is much slower than it has to be, since there’s a lot of unnecessary data being exchanged.

Now consider the same user scenario, but with the "web app" design paradigm. This flow prevents unnecessary redirects and thus feels faster and smoother to the user.

[[File:web_app_flow_2.png|center]]

First, the user lands on the movie listing website. The web server sends back static resources like HTML, JavaScript, CSS and images. Think of this as the equivalent resources that you would have in a compiled native app. These resources contain everything the web app needs to function, but it doesn’t include any dynamic data (like movie listings).

Once the browser has downloaded the static resources, it then fires an AJAX request for the API method <code>getMovies</code>. This tells the server that the browser is asking for movie listings. It then passes back only the JSON-encoded data that’s needed to show the listings,  for example:

 {
     "movies": [ 
         {"id": 34, "title": "Inception", "year": 2010},  
         {"id": 47, "title": "The Social Network", "year": 2010} 
     ]
 }

Once the browser receives this data, the JavaScript, HTML and CSS that was initially downloaded interprets the data and displays the movie listings page.

Then, the user clicks on "Inception" and the browser sends another AJAX request for this data to <code>/api?method=getMovie&id=34</code>. The server returns only the data needed to display the Inception movie page, for example:

 {
     "title": "Inception", 
     "picture": "inception.jpg", 
     "cast": [
         "Leonardo Dicaprio",
         "Ellen Page"
     ] 
 }

Again, once the browser receives this data, the JavaScript, HTML and CSS that was initially downloaded interprets the data and displays the Inception movie page.

In this flow, the user never navigates away from the first page they land on. Because of that, you can think of a web app as a "single-page website", as opposed to the traditional "multiple-page website".

== Building JSON APIs ==

For more information on building proper JSON APIs, [http://bitworking.org/news/restful_json check out this excellent guide].

Also, note that WebSockets is a newly available technology that allows real-time communication between the browser and your server. This is useful for building web apps like a chat client. For more information, see [http://www.html5rocks.com/en/tutorials/websockets/basics/ the tutorial on HTML5 Rocks] or check out [https://developer.mozilla.org/en/WebSockets the docs on the Mozilla Developer Network]. Note that support is limited, though.

Now that you have an overview of what a web app is, and you have some background on building APIs, let’s start building the web app client.

== MVC Frameworks ==

Using a Model-View-Controller (MVC) model will help you make your JavaScript code more flexible and easier to maintain. This is especially important since you’re building a web app, which will likely be handling complicated data. MVC is a design pattern that breaks a web app into three parts: the data (Model), the presentation of that data to the user (View), and the actions taken for any user interaction (Controller).

We’re not going to dive too deeply into this subject since there are great resources already available. For an excellent primer to understand how MVC works in JavaScript, see [http://www.alistapart.com/articles/javascript-mvc/ the article on A List Apart].

There are a lot of very popular JavaScript frameworks already available, but very few of them use a MVC model. However, there are a couple of burgeoning open source frameworks available.

=== [http://documentcloud.github.com/backbone/ Backbone JS] ===

Backbone JS is a lightweight MVC framework that features key-value binding, custom events,and views with declarative event handling. Typically, developers write the UI themselves or pair Backbone with other JavaScript frameworks like jQuery or Zepto (more on those below).

You can read more about it on the [http://documentcloud.github.com/backbone/ Backbone JS website], or you can check out the [https://github.com/addyosmani/backbone-fundamentals Backbone Fundamentals book].

Example web apps that use Backbone include [http://m.soundcloud.com/ SoundCloud], [http://basecamphq.com/mobile Basecamp] and [http://www.pandora.com/newpandora Pandora].

=== [http://emberjs.com/ Ember.js] ===

Ember.js is an MVC framework focused on data-centric apps. It provides a data-binding system that ensures that changes to data propagate correctly across all of the views of your web app. It also provides a standard application architecture, with built-in support for state management.

You can read more about it on [http://www.emberjs.com/ Ember's website].

A number of live web apps are actively using Ember, including [https://squareup.com/ Square], [http://www.zendesk.com/ Zendesk] and [http://livingsocial.com/ LivingSocial].

== Other Frameworks ==

The landscape of JavaScript frameworks is constantly changing; we've profiled Backbone and Ember, but there are many other frameworks to choose from, some of which [http://codebrief.com/2012/01/the-top-10-javascript-mvc-frameworks-reviewed/ are compared here].

If you're having trouble deciding which framework to use, you should check out [http://addyosmani.github.com/todomvc/ TodoMVC]. It gives example code for the same Todos app written using several different frameworks; you can compare the syntax and performance to choose what makes most sense for your app.

If you’re not interested in maintaining an MVC model, we recommend these frameworks:

=== [http://www.jQuery.com/ jQuery] ===

jQuery exposes a rich set of functions for traversing and manipulating your web app.

However, jQuery doesn’t employ a MVC model. Many developers couple it with Backbone.js to get the benefit of MVC while also getting jQuery functionality to interact with UI (e.g. traversing and manipulating the document, and animating).

You can read more about it on [http://www.jQuery.com/ jQuery's website].

Many websites use jQuery, including [http://www.technorati.com/ Technorati], [http://www.cbs.com/ CBS] and [http://www.mlb.com/ MLB].

== Mobile Frameworks ==

Mobile frameworks are specifically smaller than most frameworks so that they load fast. They may also contain mobile browser-specific functionality or workarounds.

=== [http://zeptojs.com/ Zepto] ===

Zepto is specifically built to run on mobile WebKit browsers. It’s a very small library meant to handle a lot of commonly used functionality that’s available in other frameworks like jQuery, including event chaining and document traversal and manipulation.

Zepto has been adopted by a handful of mobile web apps, including [http://basecamphq.com/mobile Basecamp] and [http://blog.linkedin.com/category/linkedin-mobile/ Linkedin].

=== [http://jquerymobile.com/ jQuery Mobile] ===

jQuery Mobile is built with a "commitment to universal accessibility" in mind; it supports [http://jquerymobile.com/demos/1.1.0/docs/about/platforms.html most platforms] and provides easy theming for your app. It is designed to be easy to learn, especially for those already familiar with jQuery.

jQuery Mobile has a great [http://jquerymobile.com/resources/ resource center] with tutorials, tools, and examples to help you get started.

Many mobile sites are using jQuery Mobile, including [http://www.slideshare.net/mobile Slideshare], [http://m.opentable.com/ OpenTable], and [https://m.box.com/ Box].

=== [http://www.sencha.com/products/touch/ Sencha Touch] ===

Like Zepto, Sencha Touch targets mobile WebKit browsers. It provides a large set of UI features aimed at helping web apps feel more native, with fast animations and smooth scrolling. 

You can read more about it on [http://www.sencha.com/products/touch/ Sencha's website].

A handful of apps are running on Sencha, including [http://www.sencha.com/apps/kivatouch/ Kiva Touch] and [http://www.sencha.com/apps/oreilly-conferences-app/ O'Reilly Conferences].
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Developer Tools, HTML, JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=Facebook HTML5 Resource Center
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}