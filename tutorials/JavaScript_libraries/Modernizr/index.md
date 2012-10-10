{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Stub
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

Modernizr runs on page load to detect the features after that it creates a JavaScript object with the result and adds classes to the html element for you to key your CSS on.

== Key Facts ==

* It tests for over 40 next-generation features, all in a matter of milliseconds
* It creates a JavaScript object (named Modernizr) that contains the results of these tests as boolean properties
* It adds classes to the html element that explain precisely what features are and are not natively supported
* It provides a script loader so you can pull in polyfills to backfill functionality in old browsers

== Install Modernizr ==

Installing the Modernizr is not the rocket engineering. It just a matter of including one JavaScript file in your head tag. Happy :)

Modernizr provide feature to build our own file also. With this feature we can build our own file with limited feature detection. [http://modernizr.com/download/ Build Modernizr]

Once you are done with the generating your custom build or full file you just need to include that file in your head section and you are done.
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_prefixed_supported=Yes
|Firefox_supported=Yes
|Firefox_version=3.5+
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=3.5+
|Internet_explorer_supported=Yes
|Internet_explorer_version=IE6+
|Internet_explorer_prefixed_supported=Yes
|Internet_explorer_prefixed_version=IE6+
|Opera_supported=Yes
|Opera_version=9.6+
|Opera_prefixed_supported=Yes
|Opera_prefixed_version=9.6+
|Safari_supported=Yes
|Safari_version=2+
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=2+
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_prefixed_supported=Yes
|Blackberry_supported=Yes
|Blackberry_version=6+
|Blackberry_prefixed_supported=Yes
|Blackberry_prefixed_version=6+
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=Yes
|Firefox_mobile_supported=Yes
|Firefox_mobile_prefixed_supported=Yes
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
{{Topics|Modernizr, Library, JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}