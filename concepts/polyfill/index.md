{{Page_Title|Polyfills for Replicating Web APIs}}
{{Flags
|High-level issues=Stub
|Content=Incomplete, Examples Needed
}}
{{API_Name}}
{{Summary_Section|Polyfills replicate browser-native APIs, so that code dependent on provided endpoints can be run in browsers that don't have them.}}
{{Concept_Page
|Content=The term "polyfill" was initially coined by Remy Sharp in 2009. Polyfills are drop-in libraries that intend to seamlessly fill browser capability gaps. "Seamlessly" meaning that they mimic the interface of the capability they are replicating as close as possible.

In addition to polyfills there also exists the category of "shims". Similar to polyfills shims also intend to bring additional capability to a browser. But they do that exposing their own proprietary interface, not replicating the official one.

Both allow you to target and tinker around with new technology which is not yet available across all commonly used browsers. So you could for example polyfill the Geolocation API in all the older IEs and then build your site around some Geolocation goodness without the IE users being left behind. 

The main difference and advantage between the two types of libraries is that with polyfills you can write your code against the official spec and then just slap in the library when a browser happens to not (yet) support it. Usually you use a so called "feature detection" to find that out. Most libraries document how to do that. Then, after a certain period of time during which people upgrade to newer browser versions, the need for the polyfill vanishes - up to the point where you can safely remove it from your code.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=Remy Sharp's [https://gist.github.com/350433 localStorage polyfill]. This simulates the Web Storage API so that (typically older) browsers can successfully execute code that depends on it.
|Code=<!DOCTYPE HTML>
<html>
<head>
<meta charset="utf-8">
<title>Polyfilling Web Storage</title>
<script>
// if browser doesn't support Web Storage, load the polyfill.
if (!window.localStorage) {
	document.write('<script src="localStorage.js"><\/script>');
}
</script>
</head>
<body>
</body>
</html>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|External_links=*[http://remysharp.com/2010/10/08/what-is-a-polyfill/ Remy Sharp - "What is a Polyfill"]
*[https://github.com/Modernizr/Modernizr/wiki/HTML5-Cross-Browser-Polyfills Modernizr's  mighty "HTML5 Cross Browser Polyfills" list]
*[http://html5please.com/#polyfill HTML5 Please's list of HTML5 features usable cross-browser with polyfills]
}}
{{Topics|Compatibility, JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}