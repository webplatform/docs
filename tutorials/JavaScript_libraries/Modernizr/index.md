{{Page_Title}}
{{Flags
|High-level issues=Stub, Missing Relevant Sections
|Content=Incomplete, Examples Best Practices
}}
{{Byline
|Name=Avinash Zala
|URL=http://www.xpertdeveloper.com
}}
{{Summary_Section|Modernizr is a JavaScript library that detects HTML5 and CSS3 features in the user’s browser.}}
{{Tutorial
|Content=== Why use Modernizr? ==

As web grows we are getting something new every day. And obviously all new features are not supported in all browsers. But some browsers like Chrome, Safari keeps updating as per the new features. So what about the browsers which don't support new features (e.g. IE7 for HTML5). Here Modernizr comes into picture. Modernizr is used to detect the browser support of any HTML5 feature.

== How it Works? ==

Modernizr runs on page load to detect the support of HTML5 and CSS3 features in the current browser; after that it creates a JavaScript object with the results, and adds classes to the <code>html</code> element for you to key your CSS on.

== Key Facts ==

* It tests for over 150 next-generation features, all in a matter of milliseconds
* It creates a JavaScript object (named Modernizr) that contains the results of these tests as boolean properties
* It adds classes to the html element that explain precisely what features are and are not natively supported
* It provides a script loader so you can pull in polyfills to backfill functionality in old browsers

== Install Modernizr ==


To install Modernizr, download a copy from [http://modernizr.com/ modernizr.com]. You can choose the Development version which includes the 40+ core tests, or [http://modernizr.com/download/ build a custom download] by picking only the features you want from the 150+ available. 

Next, you simply include the library in the <code>head</code> of your HTML page, like so:

 <script src="path/to/modernizr.js"></script>

The library will run automatically when the page loads, and make the results available to you via classes on the <code>html</code> element, and as properties on a global <code>Modernizr</code> JavaScript object, for example: 

 Modernizr.video; ''// true or false, depending on the browser's support for HTML5 video''
}}
{{Notes_Section
|Notes=There are some features that Modernizr cannot detect. See [https://github.com/Modernizr/Modernizr/wiki/Undetectables The Undetectables] on Modernizr’s wiki for more information.

Other features may yield what are known as ''false positive'' results in some browsers: the browser claims to support a feature, but its support is actually missing, broken or incomplete. Modernizr does its best to detect these false positives and will make exceptions for those cases, to offer you the most accurate feature detection available.
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=4.0+
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.5+
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=IE6+
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9.6+
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=2+
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=6+
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|JavaScript, Library}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}