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

=== PhantomJS ===

=== Mobile Browsers ===

== Setup ==

The quick brown fox

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