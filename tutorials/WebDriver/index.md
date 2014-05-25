{{Page_Title|WebDriver}}
{{Flags
|Checked_Out=No
}}
{{Byline}}
{{Summary_Section|Basic tutorial on how to use WebDriver to test web documents without using a service or 3rd party software}}
{{Tutorial
|Content=== WebDriver in a nutshell ==

WebDriver is a [https://dvcs.w3.org/hg/webdriver/raw-file/default/webdriver-spec.html W3C editors draft] for writing automated tests of websites. It aims to mimic the behaviour of a real user, and as such interacts with the HTML of the application.

All implementations of WebDriver that communicate with the browser use the [https://code.google.com/p/selenium/wiki/JsonWireProtocol JSON WireProtocol]. This wire protocol defines a RESTful web service using JSON over HTTP.

== Real world support ==

All browser vendors except of Apple are committed to the WebDriver standard. Although not all browsers provide out of the box support for it, or implement the [https://code.google.com/p/selenium/wiki/JsonWireProtocol JSON WireProtocol] as documented.

=== Microsoft Internet Explorer ===

Microsoft has Support for WebDriver via an external binary, the so called [https://code.google.com/p/selenium/wiki/InternetExplorerDriver Internet Explorer Driver] acts as a RESTful web server and instruments the browser using the non public debug API. The driver is compatible with the Internet Explorer versions 6 to 10, for IE 12 there are rumors that the WebDriver API will be brought natively to the browsers, without the need of an external binary.

=== Google Chrome ===

Google provides support for WebDriver in the same manor as Microsoft does, using an external library called [https://code.google.com/p/selenium/wiki/ChromeDriver Chromedriver], and like the Internet Explorer Driver, it acts as &quot;man in the middle&quot; to translate RESTful requests into something the browser understands. Due to the fast update path of the Chrome browser, the browser compatibility is in constant flux, but it's fairly save to say that the past three browser versions are support by the current driver binary.

=== Mozilla Firefox ===

Unfortunately Mozilla does not adhere to the WebDriver standard, but instead supports a homegrown [http://en.wikipedia.org/wiki/Transmission_Control_Protocol raw TCP socket] based testing Framework called [https://developer.mozilla.org/en-US/docs/Mozilla/QA/Marionette Marionette], which fortunately is designed to be pretty close the the WebDriver spec. It was shipped in the stable builds beginning with Firefox version 24, but itself isn't stable &amp; the API is in constant flux.

=== PhantomJS ===

PhantomJS, the [http://blog.arhg.net/2009/10/what-is-headless-browser.html headless] browser based on the WebKit rendering engine &amp; JavaScriptCore javascript engine contains a WebDriver implementation named [https://github.com/detro/ghostdriver Ghostdriver] that is nearly spec compliant. Ghostdriver is shipped bundled with PhantomJS since version 1.8.

=== Mobile Browsers ===

Mobile browsers and operation systems do not contain an native WebDriver implementation (with the exception of the FirefoxOS debug builds containing Marionette); the [http://appium.io/ Appium] project tries to fill the gap by acting as a WebDriver server for Mobile Chrome, Mobile Safari &amp; Firefox OS.

== Setup ==

For our basic test setup, we use [http://phantomjs.org/ PhantomJS] as the system we want to test &amp; Chrome as our host system which will control PhantomJS remotely. The installation of PhantomJS is straight forward, just download it from [http://phantomjs.org/download.html here] &amp; you should have the <code>phantomjs</code> binary (or the <code>phantomjs.exe</code> if you're on windows) ready.

To start the remote WebDriver server,

On *nix compatible systems:

<code>$ `./phantomjs --webdriver=8080</code>

On windows:

<code>&gt; phantomjs.exe --webdriver=8080</code>

The output should be something like this:

<code>PhantomJS is launching GhostDriver... [INFO  - 2014-05-18T12:53:19.120Z] GhostDriver - Main - running on port 8080</code>

Now that our WebDriver server is up &amp; running, we need to start our client. Lets use Google Chrome for that (we could use anything here that speaks &amp; understands HTTP as a client Node.js, PHP, other browsers etc.). Because of the <code>same origin policy</code> that all browser adhere to, we need to start Chrome with a special flag, that disables this policy for our tests, as our webdriver server runs on a different port/domain, than the page we open up in our browser.

You can disable the <code>same origin policy</code> by starting chrome with a special flag from the CMD or terminal:

On *Nix systems:

<code>open -a Google\ Chrome --args -disable-web-security -allow-file-access-from-files</code>

On Windows:

<code>chrome.exe  –allow-file-access-from-files -disable-web-security</code>

To finally check if our setup is up &amp; running, navigate to <code>localhost:8080</code>, you should see some output similar to this:

<code>
Unknown Command - Request =&gt; {&quot;headers&quot;:{&quot;Accept&quot;:&quot;text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,''/'';q=0.8&quot;,&quot;Accept-Encoding&quot;:&quot;gzip,deflate,sdch&quot;,&quot;Accept-Language&quot;:&quot;en-US,en;q=0.8,de;q=0.6&quot;,&quot;Connection&quot;:&quot;keep-alive&quot;,&quot;Host&quot;:&quot;localhost:8080&quot;,&quot;User-Agent&quot;:&quot;Mozilla/5.0 (Macintosh; Intel Mac OS X 10''9''2) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/34.0.1847.137 Safari/537.36&quot;},...]}}
</code>

== Connecting to the remote browser ==

Next step is to connect our PhantomJS based server with the JavaScript code we will run in our Chrome client instance. Lets start by creating a simple webpage that will be the host of our tests:

<pre>
&lt;!doctype html&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;meta charset=&quot;utf-8&quot;&gt;
    &lt;title&gt; WebDiver testpage&lt;/title&gt;
    &lt;meta name=&quot;description&quot; content=&quot;&quot;&gt;
    &lt;meta name=&quot;viewport&quot; content=&quot;width=device-width, initial-scale=1&quot;&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;This is a WebDiver testpage&lt;/h1&gt;
	&lt;script&gt;
	  request = new XMLHttpRequest();
	  request.open('GET', 'http://localhost:8080/status', true);

	  request.onload = function() {
	    var el = document.createElement('div');
	    var contents = document.createTextNode(request.responseText);
	      el.appendChild(contents);
	      document.getElementsByTagName('body')[0].appendChild(el);
	    };

	   request.onerror = function() {
	     // There was a connection error of some sort
	       console.error('err:', arguments);
	   };

	   request.send();
	&lt;/script&gt;
  &lt;/body&gt;
&lt;/html&gt;
</pre>

This sample page uses the <code>status</code> method defined in the [https://code.google.com/p/selenium/wiki/JsonWireProtocol JSON WireProtocol], it queries the WebDriver servers status; We take that &amp; display the contents of the request on our webpage.

The output should be something like this:

<code>{&quot;sessionId&quot;:null,&quot;status&quot;:0,&quot;value&quot;:{&quot;build&quot;:{&quot;version&quot;:&quot;1.0.4&quot;},&quot;os&quot;:{&quot;name&quot;:&quot;mac&quot;,&quot;version&quot;:&quot;unknown&quot;,&quot;arch&quot;:&quot;64bit&quot;}}}</code>

We now connected Chrome &amp; PhantomJS, time to extend our basic HTML page to obtain a WebDriver session, open up a webpage we want to test &amp; read out the title of that one.

== Browser, I command you ==

If we want to grab the title of the Webplatform Wiki main page located at <code>http://docs.webplatform.org/wiki/Main_Page</code>, we need to take three steps to make that happen:

* First, we need to get a session from the remote Webdriver (in our case, PhantomJS)
* Second, we need to tell the remote Webdriver which URL we want to navigate to
* Third and last, we need to tell the remote Webdriver which data we want, in our case, that we want the <code>title</code>

=== Obtain a session ===

As said, first we need to ask the remote Webdriver instance to start a new session for us, this is needed because a remote Webdriver instance can be requested from different clients at the same time &amp; we it needs to hold some state like which URL we are currently on for example.

To obtain a session, we need to make a <code>POST</code> request to the [https://code.google.com/p/selenium/wiki/JsonWireProtocol#/session /session] method. This method expects us to send some JSON data, the so called <code>desiredCapabilities</code>, with the request. The desired capabilities were invented to tell the remote WebDriver what we want in this run, most probably if we were running against a large browser array, which browser on which operating system we want to control. In our case, as we only want to talk directly to the browser, we can go with the default data:

<pre>{
    desiredCapabilities: {
        browserName: 'phantomjs', 
        version: '', 
        platform: 'ANY'}
}</pre>
A function that would do this request would look like this:

<pre>var getSession = function (cb) {
  var request = new XMLHttpRequest();
  request.open('POST', 'http://localhost:8080/session', true);
  request.setRequestHeader('Content-Type', 'application/json');

  request.onload = function() {
        cb(null, JSON.parse(request.responseText));
  };

  request.onerror = function() {
        cb(arguments, null);
  };

  request.send(JSON.stringify({desiredCapabilities: {browserName: 'phantomjs', version: '', platform: 'ANY'}}));
};</pre>

=== Open the URL ===

After we obtained the session, we need to tell remote browser which URL we want to open. We can do this by issuing another <code>POST</code> request to the [https://code.google.com/p/selenium/wiki/JsonWireProtocol#/session/:sessionId/url /url] method. The pattern here is always the same, if we want the remote browser to do something, like navigating to a page, clicking an element, etc., we make a <code>POST</code> request, if we want to retrieve data, we make a <code>GET</code> request.

If we transform the request into code, it looks like this:

<pre>var openUrl = function (url, session, cb) {
    var request = new XMLHttpRequest();
    request.open('POST', 'http://localhost:8080/session/' + session + '/url', true);
    request.setRequestHeader('Content-Type', 'application/json');

    request.onload = function() {
      cb(null, JSON.parse(request.responseText));
    };

    request.onerror = function() {
      cb(arguments, null);
    };

  request.send(JSON.stringify({url: url}));
};</pre>

Note that we need to send the sessionId, we received in the last request, with the request as a part of the URL. The address of the page we want to open needs to be transferred as a part of the request body.

=== Grab the title ===

Now that we know how we can control the remote browser instance, lets see how we can receive some data. As said, we want to know the title of the Webplatform.org main wiki page. In order to do so, we need to request the [https://code.google.com/p/selenium/wiki/JsonWireProtocol#/session/:sessionId/title /title] method, and as we want to receive some data, it is a <code>GET</code> request this time.

We also need to send the session with us (which makes sense, otherwise the Webdriver would not know from which URL it should fetch the title), and so the function looks quite similar to the ones we used before:

<pre>var getPageTitle = function (session, cb) {
    var request = new XMLHttpRequest();
    request.open('GET', 'http://localhost:8080/session/' + session + '/title', true);
    request.setRequestHeader('Content-Type', 'application/json');

    request.onload = function() {
        cb(null, JSON.parse(request.responseText));
    };

    request.onerror = function() {
        cb(arguments, null);
    };

    request.send();
};</pre>

=== Display title &amp; close the session ===

So, as we have coded our three functions to get a session, open an URL &amp; request the page title, it is time to glue them all together and have some fun. I hope you noticed that every of our functions above takes an argument called <code>cb</code>. <code>cb</code> is short for <code>callback</code> &amp; describes a function that should be invoked after the work in the previously called function is done, in our case, if the request is finished.

All of our callbacks take to arguments, the first argument <code>err</code> normally is <code>null</code> and will only change its value, if an error happens, in doing so we can be sure to always add at least some code to handle an error that occurs. The second arguments is the <code>data</code> that we receive from our request if it succeeds.

A typical response for a <code>GET</code> looks like this:

<pre>{
    sessionId: &quot;d8916520-e40a-11e3-84ea-b7d1dad7eee9&quot;, 
    status: 0, 
    value: &quot;WebPlatform Docs · WebPlatform Docs · WPD · WebPlatform.org&quot;
}</pre>
The response contains the <code>sessionId</code> we send with the request, a <code>status</code> that indicates if an error was risen (0 indicates success) &amp; the <code>value</code> attribute, which carries the answer to our question, in this case to: “What is the title?”. Responses for <code>POST</code> requests look similar, they only lack the <code>value</code> attribute.

Armoured with this knowledge we can glue our functions together &amp; execute them:

<pre>// load the session data
getSession(function (err, data) {
    // check for an error &amp; report
    if (err) console.error(err);
    
    // store the sessionId for later use
    var session = data.sessionId;
    
    // open the webplatform url
    openUrl('http://docs.webplatform.org/wiki/Main_Page', session, function (err, data) {
        // check for an error &amp; report
        if (err) console.error(err);
        
        // get the page title
        getPageTitle(session, function (err, data) {
            // again check for an error &amp; report
            if (err) console.error(err);
            
            // take the title response and display it
            var el = document.createElement('div');
        var contents = document.createTextNode('Title: ' + data.value);
        el.appendChild(contents);
        document.getElementsByTagName('body')[0].appendChild(el);
            
            // close the session
            closeSession(session);
        });
    });
});</pre>
You might wondered what the <code>closeSession</code> method does, that is actually a function we haven’t added yet. The <code>closeSession</code> method makes a <code>DELETE</code> request to the [https://code.google.com/p/selenium/wiki/JsonWireProtocol#DELETE_/session/:sessionId /session] method, which terminates the session (otherwise it would be open for a long time before it times out).

The function to do this, looks like so:

<pre>var closeSession = function (session) {
  var request = new XMLHttpRequest();
  request.open('DELETE', 'http://localhost:8080/session/' + session, true);
  request.setRequestHeader('Content-Type', 'application/json');
  request.send();           
};</pre>

== Summary ==

To sum it up, the complete code looks like this:

<pre>&lt;!doctype html&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;meta charset=&quot;utf-8&quot;&gt;
    &lt;title&gt; WebDiver testpage&lt;/title&gt;
    &lt;meta name=&quot;description&quot; content=&quot;&quot;&gt;
    &lt;meta name=&quot;viewport&quot; content=&quot;width=device-width, initial-scale=1&quot;&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;This is a WebDiver testpage&lt;/h1&gt;
        &lt;script&gt;
            var getSession = function (cb) {
              var request = new XMLHttpRequest();
              request.open('POST', 'http://localhost:8080/session', true);
              request.setRequestHeader('Content-Type', 'application/json');
            
              request.onload = function() {
                    cb(null, JSON.parse(request.responseText));
              };

              request.onerror = function() {
                    cb(arguments, null);
              };

              request.send(JSON.stringify({desiredCapabilities: {browserName: 'phantomjs', version: '', platform: 'ANY'}}));
            };
            
            var openUrl = function (url, session, cb) {
                var request = new XMLHttpRequest();
                request.open('POST', 'http://localhost:8080/session/' + session + '/url', true);
                request.setRequestHeader('Content-Type', 'application/json');

                request.onload = function() {
                  cb(null, JSON.parse(request.responseText));
                };

                request.onerror = function() {
                  cb(arguments, null);
                };

              request.send(JSON.stringify({url: url}));
            };
            
            var getPageTitle = function (session, cb) {
                var request = new XMLHttpRequest();
                request.open('GET', 'http://localhost:8080/session/' + session + '/title', true);
                request.setRequestHeader('Content-Type', 'application/json');

                request.onload = function() {
                    cb(null, JSON.parse(request.responseText));
                };

                request.onerror = function() {
                    cb(arguments, null);
                };

                request.send();
            };
            
            var closeSession = function (session) {
              var request = new XMLHttpRequest();
              request.open('DELETE', 'http://localhost:8080/session/' + session, true);
              request.setRequestHeader('Content-Type', 'application/json');
              request.send();           
            };
            
            // the fun part
            getSession(function (err, data) {
                if (err) console.error(err);
                
                var session = data.sessionId;
                openUrl('http://docs.webplatform.org/wiki/Main_Page', session, function (err, data) {
                    if (err) console.error(err);
                    
                    getPageTitle(session, function (err, data) {
                        if (err) console.error(err);
                        
                        var el = document.createElement('div');
                    var contents = document.createTextNode('Title: ' + data.value);
                    el.appendChild(contents);
                    document.getElementsByTagName('body')[0].appendChild(el);
                
                        closeSession(session);
                    });
                });
            });
        &lt;/script&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

I encourage you to take this as a foundation, to play around with &amp; to gain even more and deeper knowledge on how Webdriver works.

== Further reading &amp; tooling ==

* [https://dvcs.w3.org/hg/webdriver/raw-file/default/webdriver-spec.html W3C editors draft] - The W3Cs specification document on Webdriver
* [https://code.google.com/p/selenium/wiki/JsonWireProtocol JSON WireProtocol] - The JSON WireProtocol specification
* [http://docs.seleniumhq.org/ Selenium] - A Java based Framework to interface with different browsers
* [http://appium.io/ Appium] - A Node.js based framework to interface with mobile applications &amp; browsers
* [https://github.com/admc/wd WD.js] - A Node.js framework to interface with different browsers
* [http://dalekjs.com/ Dalek.js] - A Node.js framework designed to test websites in different browsers
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
}





}