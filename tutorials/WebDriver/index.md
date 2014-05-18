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

<code>open -a Google\ Chrome --args --disable-web-security -–allow-file-access-from-files</code>

On Windows:

<code>chrome.exe  –allow-file-access-from-files -disable-web-security</code>

To finally check if our setup is up &amp; running, navigate to <code>localhost:8080</code>, you should see some output similar to this:

``` Unknown Command - Request =&gt; {&quot;headers&quot;:{&quot;Accept&quot;:&quot;text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,''/'';q=0.8&quot;,&quot;Accept-Encoding&quot;:&quot;gzip,deflate,sdch&quot;,&quot;Accept-Language&quot;:&quot;en-US,en;q=0.8,de;q=0.6&quot;,&quot;Connection&quot;:&quot;keep-alive&quot;,&quot;Host&quot;:&quot;localhost:8080&quot;,&quot;User-Agent&quot;:&quot;Mozilla/5.0 (Macintosh; Intel Mac OS X 10''9''2) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/34.0.1847.137 Safari/537.36&quot;},&quot;httpVersion&quot;:&quot;1.1&quot;,&quot;method&quot;:&quot;GET&quot;,&quot;url&quot;:&quot;/&quot;,&quot;urlParsed&quot;:{&quot;anchor&quot;:&quot;&quot;,&quot;query&quot;:&quot;&quot;,&quot;file&quot;:&quot;&quot;,&quot;directory&quot;:&quot;/&quot;,&quot;path&quot;:&quot;/&quot;,&quot;relative&quot;:&quot;/&quot;,&quot;port&quot;:&quot;&quot;,&quot;host&quot;:&quot;&quot;,&quot;password&quot;:&quot;&quot;,&quot;user&quot;:&quot;&quot;,&quot;userInfo&quot;:&quot;&quot;,&quot;authority&quot;:&quot;&quot;,&quot;protocol&quot;:&quot;&quot;,&quot;source&quot;:&quot;/&quot;,&quot;queryKey&quot;:{},&quot;chunks&quot;:[&quot;&quot;]}}

== Connecting to the remote browser ==

The quick brown fox

== Simple test case ==

The quick brown fox

== Summary ==

The quick brown fox

== Further reading &amp; tooling ==

The quick brown fox
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
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