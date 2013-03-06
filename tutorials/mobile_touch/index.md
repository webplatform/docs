{{Page_Title|Introduction to multi-touch Web development}}
{{Flags
|High-level issues=Needs Flags
}}
{{Byline
|Name=Boris Smus
|URL=http://www.html5rocks.com/profiles/#smus
|Published=Aug. 21, 2011
}}
{{Summary_Section|An introduction to multi-touch mobile web development.}}
{{Tutorial
|Content===Introduction==

Mobile devices such as smartphones and tablets usually have a capacitive touch-sensitive screen to capture interactions made with the user's fingers. As the mobile web evolves to enable increasingly sophisticated applications, web developers need a way to handle these events. For example, nearly any fast-paced game requires the player to press multiple buttons at once which, in the context of a touchscreen, implies multi-touch.

Apple introduced their [http://developer.apple.com/library/safari/#documentation/UserExperience/Reference/TouchEventClassReference/TouchEvent/TouchEvent.html#//apple_ref/doc/uid/TP40009358 touch events API] in iOS 2.0. Android has been catching up to this de-facto standard and closing the gap. Recently a W3C working group has come together to work on this [http://dvcs.w3.org/hg/webevents/raw-file/tip/touchevents.html touch events specification].

In this article I'll dive into the touch events API provided by iOS and Android devices, explore what sorts of applications you can build, present some best practices, and cover useful techniques that make it easier to develop touch-enabled applications.

==Touch events==

Three basic touch events are outlined in the spec and implemented widely across mobile devices:

* <code>touchstart</code>: a finger is placed on a DOM element.
* <code>touchmove</code>: a finger is dragged along a DOM element.
* <code>touchend</code>: a finger is removed from a DOM element.

Each touch event includes three lists of touches:

* <code>touches</code>: a list of all fingers currently on the screen.
* <code>targetTouches</code>: a list of fingers on the current DOM element.
* <code>changedTouches</code>: a list of fingers involved in the current event. For example, in a touchend event, this will be the finger that was removed.

These lists consist of objects that contain touch information:

* <code>identifier</code>: a number that uniquely identifies the current finger in the touch session.
* <code>target</code>: the DOM element that was the target of the action.
* <code>client/page/screen coordinates</code>: where on the screen the action happened.
* <code>radius coordinates and rotationAngle</code>: describe the ellipse that approximates finger shape.

==Touch-enabled apps==

The <code>touchstart</code>, <code>touchmove</code>, and <code>touchend</code> events provide a rich enough feature set to support virtually any kind of touch-based interaction, including all of the usual multi-touch gestures like pinch-zoom, rotation, and so on.

This snippet lets you drag a DOM element around using single-finger touch:

<pre>
 var obj = document.getElementById('id');
 obj.addEventListener('touchmove', function(event) {
   // If there's exactly one finger inside this element
   if (event.targetTouches.length == 1) {
     var touch = event.targetTouches[0];
     // Place element where the finger is
     obj.style.left = touch.pageX + 'px';
     obj.style.top = touch.pageY + 'px';
   }
 }, false);
</pre>

Below is a [https://github.com/borismus/MagicTouch/blob/master/samples/tracker.html sample] that displays all current touches on the screen. It's useful just to get a feeling for the responsiveness of the device.

[https://github.com/borismus/MagicTouch/blob/master/samples/tracker.html [[Image:mtfinger.jpg]] ]<br/>
[https://github.com/borismus/MagicTouch/blob/master/samples/tracker.html Touch tracker]

<pre>
 // Set up canvas and expose context via ctx variable
 canvas.addEventListener('touchmove', function(event) {
   for (var i = 0; i < event.touches.length; i++) {
     var touch = event.touches[i];
     ctx.beginPath();
     ctx.arc(touch.pageX, touch.pageY, 20, 0, 2*Math.PI, true);
     ctx.fill();
     ctx.stroke();
   }
 }, false);
</pre>

===Demos===

A number of interesting multi-touch demos are already in the wild, such as this [http://paulirish.com/demo/multi canvas-based drawing] demo by Paul Irish and others.

[http://paulirish.com/demo/multi [[Image:mtdraw.jpg]] ]<br/>
[http://paulirish.com/demo/multi Drawing demo]

And [http://smus.com/x/browser-ninja/ Browser Ninja], a tech demo that is a Fruit Ninja clone using CSS3 transforms and transitions, as well as canvas.

[http://smus.com/x/browser-ninja  [[Image:mtninja.jpg]] ]<br/>
[http://smus.com/x/browser-ninja Browser ninja]

==Best practices==

===Prevent zooming===

Default settings don't work very well for multi-touch, because your swipes and gestures are often associated with browser behavior, such as scrolling and zooming.

To disable zooming, set up your viewport so that it is not user-scalable using the following meta tag:

<pre>
 <meta name="viewport"
   content="width=device-width, initial-scale=1.0, user-scalable=no">
</pre>

Check out [http://www.html5rocks.com/mobile/mobifying.html#toc-meta-viewport this mobile HTML5 article] for more information on setting up your viewport.

===Prevent scrolling===

Some mobile devices have default behaviors for <code>touchmove</code>, such as the classic iOS overscroll effect, which causes the view to bounce back when scrolling exceeds the bounds of the content. This is confusing in many multi-touch applications, and can easily be disabled:

<pre>
 document.body.addEventListener('touchmove', function(event) {
   event.preventDefault();
 }, false);
</pre>

===Render carefully===

If you are writing a multi-touch application that involves complex multi-finger gestures, be careful how you react to touch events, because you will be handling so many at once. Consider the sample in the previous section that draws all touches on the screen. You could draw as soon as there is a touch input:

<pre>
 canvas.addEventListener('touchmove', function(event) {
   renderTouches(event.touches);
 }, false);
</pre>

But this technique does not scale with number of fingers on the screen. Instead, you could track all of the fingers, and render in a loop to get far better performance:

<pre>
 var touches = []
 canvas.addEventListener('touchmove', function(event) {
   touches = event.touches;
 }, false);
 
 // Setup a 60fps timer
 timer = setInterval(function() {
   renderTouches(touches);
 }, 15);
</pre>

'''Tip:''' <code>setInterval</code> is not great for animations, because it doesn't take into account the browser's own rendering loop. Modern desktop browsers provide [http://www.html5rocks.com/tutorials/speed/html5/#toc-request-ani-frame requestAnimationFrame], which is a much better option for performance and battery life reasons. Once supported in mobile browsers, this will be the preferred way of doing things.

===Make use of targetTouches and changedTouches===

Remember that <code>event.touches</code> is an array of ''all'' fingers in contact with the screen, not just the ones on the DOM element's target. You might find it more useful to use <code>event.targetTouches</code> or <code>event.changedTouches</code> instead.

Finally, because you are developing for mobile, you should be aware of general mobile best practices, which are covered in [http://www.html5rocks.com/mobile/mobifying.html Eric Bidelman's article], as well as this [http://www.w3.org/TR/mwabp/ W3C document].

==Device support==

''(Ed. note: This section contains useful information, but may be out of date. See the compatibility tables at the end of this article for more current information.)''

Unfortunately, touch event implementations vary greatly in completeness and quality. I wrote a [https://github.com/borismus/MagicTouch/blob/master/index.html diagnostics script] that displays some basic information about the touch API implementation, including which events are supported and <code>touchmove</code> firing resolution. I tested Android 2.3.3 on Nexus One and Nexus S hardware, Android 3.0.1 on Xoom, and iOS 4.2 on iPad and iPhone.

In a nutshell, all tested browsers support the <code>touchstart</code>, <code>touchend</code>, and <code>touchmove</code> events.

The spec provides three additional touch events, but no tested browsers support them:

* <code>touchenter</code>: a moving finger enters a DOM element.
* <code>touchleave</code>: a moving finger leaves a DOM element.
* <code>touchcancel</code>: a touch is interrupted (implementation specific).

Within each touch list, the tested browsers also provide the <code>touches</code>, <code>targetTouches</code> and <code>changedTouches</code> touch lists. However, no tested browsers support <code>radiusX</code>, <code>radiusY</code>, or <code>rotationAngle</code>, which specify the shape of the finger touching the screen.

During a <code>touchmove</code>, events fire roughly 60 times a second across all tested devices.

===Android 2.3.3 (Nexus)===

On the Android Gingerbread Browser (tested on Nexus One and Nexus S), there is no multi-touch support. This is a [http://code.google.com/p/android/issues/detail?id=11909 known issue].

===Android 3.0.1 (Xoom)===

On Xoom's browser, there is basic multi-touch support, but it only works on a single DOM element. The browser does not correctly respond to two simultaneous touches on different DOM elements. In other words, the following will react to two simultaneous touches:

<pre>
 obj1.addEventListener('touchmove', function(event) {
   for (var i = 0; i < event.targetTouches; i++) {
     var touch = event.targetTouches[i];
     console.log('touched ' + touch.identifier);
   }
 }, false);
</pre>

But the following will not:

<pre>
 var objs = [obj1, obj2];
 for (var i = 0; i < objs.length; i++) {
   var obj = objs[i];
   obj.addEventListener('touchmove', function(event) {
     if (event.targetTouches.length == 1) {
       console.log('touched ' + event.targetTouches[0].identifier);
     }
   }, false);
 }
</pre>

===iOS 4.x (iPad, iPhone)===

iOS devices fully support multi-touch, are capable of tracking quite a few fingers and provide a very responsive touch experience in the browser.

===Internet Explorer 10===

Internet Explorer does not have touch events. Instead Microsoft implemented pointer events in IE10 and suggested it as a new [http://www.w3.org/TR/pointerevents/ spec] to the W3C. See [http://docs.webplatform.org/wiki/concepts/PointerEvents PointerEvents] for more info.

==Developer tools==

In mobile development, it's often easier to start prototyping on the desktop and then tackle the mobile-specific parts on the devices you intend to support. Multi-touch is one of those features that's difficult to test on the PC, since most PCs don't have touch input.

Having to test on mobile can lengthen your development cycle, since every change you make must be pushed out to a server and then loaded on the device. Then, once running, there is little you can do to debug your application, as tablets and smartphones lack web developer tooling.

A solution to this problem is to simulate touch events on your development machine. For single-touches, touch events can be simulated based on mouse events. Multi-touch events can be simulated if you have a device with touch input, such as a modern Apple MacBook.

===Single-touch events===

If you would like to simulate single-touch events on your desktop, try out [http://www.vodori.com/blog/phantom-limb.html Phantom Limb], which simulates touch events on pages and also gives a giant hand to boot.

There's also the [https://github.com/dotmaster/Touchable-jQuery-Plugin Touchable] jQuery plugin that unifies touch and mouse events across platforms.

===Multi-touch events===

To enable your multi-touch web application to work in your browser on your multi-touch trackpad (such as a Apple MacBook or MagicPad), I've created the [http://github.com/borismus/MagicTouch MagicTouch.js polyfill]. It captures touch events from your trackpad and turns them into standard-compatible touch events. To use it:

# Download and install the [https://github.com/fajran/npTuioClient npTuioClient NPAPI plugin] into ~/Library/Internet Plug-Ins/.
# Download the [https://github.com/fajran/tongseng TongSeng TUIO app] for Macs MagicPad and start the server.
# Download [http://github.com/borismus/MagicTouch MagicTouch.js], a javascript library to simulate spec-compatible touch events based on npTuioClient callbacks.
# Include the magictouch.js script and npTuioClient plugin in your application as follows:

<pre>
 <head>
   ...
   <script src="/path/to/magictouch.js"></script>
 </head>
 
 <body>
   ...
   <object id="tuio" type="application/x-tuio" style="width: 0px; height: 0px;">
     Touch input plugin failed to load!
   </object>
 </body>
</pre>

I tested this approach only with Chrome, but it should work on other modern browsers with only minor tweaks.

If your computer does not have multi-touch input, you can simulate touch events using other TUIO trackers, such as [http://reactivision.sourceforge.net/ reacTIVision]. For more information, see the [http://www.tuio.org/ TUIO project page].

Note that your gestures might be identical to OS-level multi-touch gestures. On OS X, you can configure system-wide events by going to the Trackpad preference pane in System Preferences.

As multi-touch features become more widely supported across mobile browsers, I'm very excited to see new web applications take full advantage of this rich API.
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Touch events
|Chrome_supported=Yes
|Chrome_version=22
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=12.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=16
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=6
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=11.0
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Pointer Events
}}
{{Topics|Mobile, Touch}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=http://www.html5rocks.com/mobile/touch/
}}