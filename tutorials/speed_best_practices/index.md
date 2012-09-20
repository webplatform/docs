{{Flags
|High-level issues=Needs Flags
|Compatibility=Incomplete
}}
{{Summary_Section|Tips to improve HTML5 web app performance.}}
{{Tutorial
|Content==Best Practices for a Faster Web App with HTML5=
====original by Paul Irish====
====published June 18, 2010====

==Introduction==

Much of HTML5 aims to deliver native browser support for components and techniques that we have achieved through JavaScript libraries thus far. Using these features, when present, can end up delivering a much faster experience for your users. In this tutorial, we won't recap the excellent performance research that you've seen at Yahoo's [http://developer.yahoo.com/performance/rules.html Exceptional Performance site] or Google's [http://code.google.com/speed/page-speed/docs/rules_intro.html Page Speed docs] and [http://code.google.com/speed/index.html Let's make the web faster] sites. Instead we'll focus on how putting HTML5 and CSS3 to use today can make your web apps more responsive.

==Tip 1: Use web storage in place of cookies==

While cookies have been used to track unique user data for years, they have serious disadvantages. The largest flaw is that all of your cookie data is added to every HTTP request header. This can end up having a [http://yuiblog.com/blog/2007/03/01/performance-research-part-3/ measurable impact on response time], especially during XHRs. So a best practice is to [http://developer.yahoo.com/performance/rules.html#cookie_size reduce cookie size]. In HTML5 we can do better than that: use <code>sessionStorage</code> and <code>localStorage</code> in place of cookies.

These two web storage objects can be used, respectively, to persist user data on the client side for the length of the session or indefinitely. Their data is not transferred to the server via every HTTP request, either. They have an API that will make you happy to be rid of cookies. Here are both APIs, using cookies as a fallback.

<pre>
 // if localStorage is present, use that
 if (('localStorage' in window) &amp;&amp; window.localStorage !== null) {
 
   // easy object property API
   localStorage.wishlist = '["Unicorn","Narwhal","Deathbear"]';
 
 } else {
 
   // without sessionStorage we'll have to use a far-future cookie
   //   with document.cookie's awkward API :(
   var date = new Date();
   date.setTime(date.getTime()+(365*24*60*60*1000));
   var expires = date.toGMTString();
   var cookiestr = 'wishlist=["Unicorn","Narwhal","Deathbear"];'+
                   ' expires='+expires+'; path=/';
   document.cookie = cookiestr;
 }
</pre>

==Tip 2: Use CSS Transitions instead of JavaScript animation==

CSS Transitions give you an attractive visual transition between two states. Most style properties can be transitioned, like manipulating the text-shadow, position, background, or color. You can use transitions into pseudo-selector states like <code><nowiki>:hover</nowiki></code> or from HTML5 forms, <code><nowiki>:invalid</nowiki></code> and <code><nowiki>:valid</nowiki></code> ([http://bradshawenterprises.com/tests/formdemo.php example with form validation states]). But they're much more powerful and can be triggered when you add any class to an element.

<pre>
 div.box {
   left: 40px;
   -webkit-transition: all 0.3s ease-out;
      -moz-transition: all 0.3s ease-out;
        -o-transition: all 0.3s ease-out;
           transition: all 0.3s ease-out;
 }
 div.box.totheleft { left: 0px; }
 div.box.totheright { left: 80px; }
</pre> 

By adding the toggling the classes of <code>totheleft</code> and <code>totheright</code> you can move the box around. Compare this amount of code with that of a JavaScript animation library. Clearly, the number of bytes sent to the browser is much less when using CSS-based animation. Additionally, with GPU level acceleration, these visual transitions will be as smooth as possible.

==Tip 3: Use client-side databases instead of server roundtrips==

[http://dev.w3.org/html5/webdatabase/ Web SQL Database] and [http://www.w3.org/TR/IndexedDB/ IndexedDB] introduce databases to the client side. Instead of the common pattern of posting data to the server via <code>XMLHttpRequest</code> or form submission, you can leverage these client-side databases. Decreasing HTTP requests is a primary target of all performance engineers, so using these as a datastore can save many trips via XHR or form posts back to the server. <code>localStorage</code> and <code>sessionStorage</code> could be used in some cases, like capturing form submission progress, and have been seen to be noticeably faster than the client-side database APIs.

For example, if you have a data grid component or an inbox with hundreds of messages, storing the data locally in a database will save you HTTP roundtrips when the user wishes to search, filter, or sort. A list of friends or a text input autocomplete could be filtered on each keystroke, making for a much more responsive user experience. Certainly view the [/tutorials/webdatabase/todo/ Web SQL Database tutorial] for a comprehensive guide at putting this to work.

==Tip 4: JavaScript improvements lend considerable performance advantages==

Many [https://developer.mozilla.org/En/Core_JavaScript_1.5_Reference/Objects/Array#Methods additional methods were added to the Array protoype] in JavaScript 1.6. For example:

<pre>
 // Give me a new array of all values multiplied by 10.
 [5, 6, 7, 8, 900].map(function(value) { return value * 10; });
 // [50, 60, 70, 80, 9000]
 
 // Create links to specs and drop them into #links.
 ['html5', 'css3', 'webgl'].forEach(function(value) {
   var linksList = document.querySelector('#links');
   var newLink = value.link('http://google.com/search?btnI=1&amp;q=' + value + ' spec');
   linksList.innerHTML +=  newLink;
 });
 
 // Return a new array of all mathematical constants under 2.
 [3.14, 2.718, 1.618].filter(function(number) {
   return number &lt; 2;
 });
 // [1.618]
 
 // You can also use these extras on other collections like nodeLists.
 [].forEach.call(document.querySelectorAll('section[data-bucket]'), function(elem, i) {
   localStorage['bucket' + i] = elem.getAttribute('data-bucket');
 });
</pre>

In most cases, these native methods yield significantly faster speeds than your typical <code>for</code> loop like: <code>for (var i = 0, len = arr.length; i &lt; len; i++)</code>.

Native JSON parsing (via <code>JSON.parse()</code>) replaces the json2.js file we've been used to including for a while. Native JSON is much faster and safer than using an external script.

Native <code>String.trim</code> is another good example of being not only faster than the longhand JS equivalents, but also potentially more correct. None of these JavaScript additions are technically HTML5, but they fall within the umbrella of technologies that are now becoming available.

==Tip 5: Use cache manifest for live sites, not just offline apps==

Two years back, Wordpress used Google Gears to add a feature called [http://en.blog.wordpress.com/2008/07/02/gears/ Wordpress Turbo]. It essentially cached many of the resources used in the admin panel locally, speeding up file access to them. We can replicate that behavior with HTML5's applicationCache and the [http://www.whatwg.org/specs/web-apps/current-work/multipage/offline.html#manifests cache.manifest].

The app cache has a slight advantage over setting <code>Expires</code> headers; because you make a declarative file indicating the static resources that can be cacheable, browsers can optimize that heavily, perhaps even precaching them ahead of your use.

Consider your site's basic structure as a template. You have data that may change but the HTML around it typically remains pretty consistent. With the app cache you could treat your HTML as a series of pure templates, cache the markup via the cache.manifest, and then deliver JSON over the wire to update the content. This model is very similar to what an iPhone or Android native news app does.

Read the [http://www.html5rocks.com/tutorials/appcache/beginner/ application cache tutorial] for a guide on putting this to use.

==Tip 6: Enable hardware acceleration to enhance visual experience==

In leading browsers, many visual operations can leverage GPU-level acceleration, which can make highly dynamic visual operations much smoother. Hardware acceleration has been announced for [http://www.basschouten.com/blog1.php/2010/03/02/presenting-direct2d-hardware-acceleratio Firefox Minefield] and [http://blogs.msdn.com/b/ie/archive/2010/03/16/html5-hardware-accelerated-first-ie9-platform-preview-available-for-developers.aspx IE9] and Safari added hardware-level acceleration in version 5. (It arrived in Mobile Safari much earlier.) Chromium has [http://groups.google.com/group/chromium-dev/browse_thread/thread/291aa79568684c70 just added] 3D transforms and hardware acceleration for Windows, with the other two platforms coming soon.

GPU acceleration kicks in only under a fairly restricted set of conditions, but 3D transforms and animated opacity are the most common ways to trip the switch. A somewhat hacky but unobtrusive way to turn it on is:

<pre>
   .hwaccel { -webkit-transform: translateZ(0); }
</pre>

No guarantees, though. :)

With hardware acceleration supported and enabled, animated translation, rotation, scaling, and opacity will definitely be smoother with GPU compositing. They have the benefit of being handled directly on the GPU and don't require redrawing of the layer contents. However, any property that affects the layout of the page will still be ''relatively'' slow.

==Tip 7: For CPU-heavy operations, Web Workers deliver==

Web Workers have two significant benefits: 1) They are fast. 2) While they chug on your tasks, the browser remains responsive. Grab a look at the [http://slides.html5rocks.com/#web-workers HTML5 Slide Deck] for Workers in action.

Some possible situations where you could use Web Workers:

* Text formatting of a long document
* Syntax highlighting
* Image processing
* Image synthesis
* Processing large arrays

==Tip 8: HTML5 Form attributes and input types==

HTML5 introduces a new set of input types, upgrading our set of <code>text</code>, <code>password</code>, and <code>file</code> to include <code>search</code>, <code>tel</code>, <code>url</code>, <code>email</code>, <code>datetime</code>, <code>date</code>, <code>month</code>, <code>week</code>, <code>time</code>, <code>datetime-local</code>, <code>number</code>, <code>range</code>, and <code>color</code>. Browser support for these varies, with Opera implementing most at the moment. With feature detection you can determine if the browser has native support (and will offer a UI like a datepicker or color picker) and, if not, you can continue to use the JS widgets to accomplish these common tasks.

In addition to the types, a few useful features have been added to our normal input fields. The input <code>placeholder</code> offers default text that clears when you click into a field, and <code>autofocus</code> focuses the caret on page load so you can interact immediately with that field. Input validation is another thing making its way in with HTML5. Adding the <code>required</code> attribute means the browser won't let the form be submitted until that field is filled in. Also, the <code>pattern</code> attribute lets you specify a custom regular expression for the input to be tested against, with invalid values blocking form submission. This declarative syntax is a big upgrade not only in source readability but is also a significant reduction in the amount of JavaScript necessary. Again, you can use feature detection to serve a fallback solution if native support for these features is not present.

Using the native widgets here means you don't need to send the heavy JavaScript and CSS required to pull off these widgets, speeding up page load and likely improving widget responsiveness. To try out some of these input enhancements, check out the [http://slides.html5rocks.com/#new-form-types HTML5 Slide deck].

==Tip 9: Use CSS3 effects instead of requesting heavy image sprites==

CSS3 delivers many new styling possibilities that supplant our use of images to represent the visual design accurately. Replacing a 2k image with 100 bytes of CSS is a huge win&mdash;not to mention you've removed yet another HTTP request. A few of the properties to familiarize yourself with are:

* Linear and radial gradients
* Border-radius for rounded corners
* Box-shadow for drop shadows and glow
* RGBA for alpha opacity
* Transforms for rotation
* CSS masks

For example, you can create very [http://cubiq.org/dropbox/cssgrad.html polished buttons via gradients] and [http://www.phpied.com/css-performance-ui-with-fewer-images/ replicate many other effects] sans images. Browser support for most of these is very solid, and you can use a library like [http://www.modernizr.com/ Modernizr] to catch browsers that don't support the features in order to use images in a fallback case.

==Tip 10: WebSockets for faster delivery with less bandwidth than XHR==

[http://dev.w3.org/html5/websockets/ WebSockets] was designed in response to the growing popularity of [http://en.wikipedia.org/wiki/Comet_(programming) Comet]. There are indeed advantages to using WebSockets now, instead of the Comet-over-XHR model.

WebSockets has very light framing, so the bandwidth it consumes is often lighter than that of XHR. [http://axod.blogspot.com/2009/12/websocket-some-numbers.html Some reports] indicate a 35% reduction in bytes sent across the wire. Additionally, in higher volume the performance difference when it comes to message delivery is more apparent; XHR has been recorded [http://bloga.jp/ws/jq/wakachi/mecab/wakachi.html in this test] as having an aggregate time of 3500% longer than WebSockets. Lastly, [http://www.youtube.com/watch?v=Z897fkPn7Rw Ericsson Labs considered the performance of WebSockets] and found the ping times over HTTP were 3-5 times larger than over WebSockets due to more substantial processing requirements. They concluded that the WebSocket protocol was clearly more suitable for realtime applications.

==Additional Resources==

For measurement and performance recommendations, you should certainly be using the Firefox extensions [http://code.google.com/speed/page-speed/ Page Speed] and [http://developer.yahoo.com/yslow/ YSlow]. Additionally, [http://code.google.com/webtoolkit/speedtracer/ Speed Tracer for Chrome] and [http://ajax.dynatrace.com/pages/ DynaTrace Ajax for IE] provide a more detailed level of logging of analysis.

The [http://www.html5rocks.com/tutorials/developertools/part1/ guide to Chrome's Developer Tools] should help orient you with the resources tab and will soon cover the [http://webkit.org/blog/1091/more-web-inspector-updates/#audits_panel new Audits panel].
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Web Storage
|Chrome_supported=Yes
|Chrome_version=20
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=12
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=8
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
|Feature=CSS Transitions
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=20
|Firefox_supported=Yes
|Firefox_version=16
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=12
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.1
|Opera_prefixed_supported=Yes
|Opera_prefixed_version=12.0
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=5.1
}}{{Compatibility Table Desktop Row
|Feature=Web SQL Database
|Chrome_supported=Yes
|Chrome_version=20.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=IndexedDB
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=20.0
|Firefox_supported=Yes
|Firefox_version=16.0
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=12.0
|Internet_explorer_supported=Yes
|Internet_explorer_version=10.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=JSON Parsing
|Chrome_supported=Yes
|Chrome_version=20.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=12.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=8.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=Offline Web Applications
|Chrome_supported=Yes
|Chrome_version=20.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=12.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=Web Storage
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_phone_supported=Unknown
|IE_phone_version=
|IE_phone_prefixed_supported=Unknown
|IE_phone_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=12
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=CSS Transitions
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Yes
|Android_prefixed_version=2.1
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_phone_supported=Unknown
|IE_phone_version=
|IE_phone_prefixed_supported=Unknown
|IE_phone_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Yes
|Safari_mobile_prefixed_version=3.2
}}{{Compatibility Table Mobile Row
|Feature=Web SQL Database
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_phone_supported=Unknown
|IE_phone_version=
|IE_phone_prefixed_supported=Unknown
|IE_phone_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=IndexedDB
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_phone_supported=Unknown
|IE_phone_version=
|IE_phone_prefixed_supported=Unknown
|IE_phone_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=JSON Parsing
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_phone_supported=Unknown
|IE_phone_version=
|IE_phone_prefixed_supported=Unknown
|IE_phone_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=5.0
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=4.0
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=Offline Web Applications
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_phone_supported=Unknown
|IE_phone_version=
|IE_phone_prefixed_supported=Unknown
|IE_phone_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Developer Tools, Performance}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=http://www.html5rocks.com/en/tutorials/speed/quick/
}}