{{Page_Title|Using device orientation}}
{{Flags
|High-level issues=Needs Flags
}}
{{Byline
|Name=Pete LePage
|URL=http://www.html5rocks.com/profiles/#petele
}}
{{Summary_Section|An introduction to using device orientation events.}}
{{Tutorial
|Content==This End Up: Using Device Orientation=

 [/profiles/#petele [[Image:xpetele.75.png.pagespeed.ic.IxfSzPUgZP.jpg{{!}}75px{{!}}Pete LePage]]]

==By '''[http://www.html5rocks.com/profiles/#petele Pete LePage]'''==

==Introduction==

Many new computers, mobile phones, and other devices are now shipping standard with accelerometers, gyroscopes, compasses, and other hardware designed to determine and capture motion and orientation data. At the same time, web browsers are providing increasingly more access to that new hardware. Examples of that are the new [http://dev.w3.org/geo/api/spec-source-orientation HTML5 DeviceOrientation and DeviceMotion events]. These events provide developers with information about the orientation, motion, and acceleration of the device.

These events have a lot of fun uses, such as using orientation to control the direction of character in a game, or motion to determine how high a character should jump. Additionally, you can use these events beyond gaming. When used with GeoLocation, you can create a more accurate turn-by-turn navigation system.

In this article, we’ll take a look at three different events, and use CSS to rotate an image based on the orientation of the device.

==Which end is up?==

There are a couple of things that we need to make sure we understand before we can start using these events: which end is up, and what are the axes we’re going to use?

The easiest way to answer the first question is to take your device and put it on flat, level surface in its “resting” position, the position it will be most stable in. For a mobile phone, that’s probably on the table, with the screen facing up and the the bottom of the phone closest to you. For a laptop, that's probably on a deck with its screen open facing you, and the keyboard in line with the surface.

[[Image:up01.png]]<br/>
''Phone is in its normal position, on a flat on surface, with the screen facing up and the bottom of the phone closest to you. The x, y, and z values increase as you move to the right, forward, or up, respectively''

Acceleration data is returned as a coordinate frame with three axes, x, y, and z. The x-axis runs side-to-side across the mobile phone screen or the laptop keyboard and is positive toward the right side. The y-axis runs front-to-back across the mobile phone screen or the laptop keyboard and is positive as it moves away from you. The z-axis comes straight up out of the mobile phone screen or the laptop keyboard and is positive as it moves up.

[[Image:up02.png]]<br/>
''The phone is rotated on the y-axis by gamma degrees''

The rotation data uses Euler angles to represent the difference between the device in its normal position and its current position. With the HTML5 device orientation events, the data is returned as the number of degrees different from normal. An easier way to think about it is how much the device is tilted side-to-side, usually referred to as beta, how much it is tilted front-to-back, known as gamma, and how much it is rotated around the z-axis, known as alpha.

One thing to keep in mind is that most people don’t use their phones when they’re in this flat position, and instead have rotated them around the x-axis so the screen is facing them. This will affect the acceleration data that is returned from the device motion events.

==The events==

===Device orientation===

The device orientation event returns only the rotation data, which includes how much the device is leaning side-to-side (beta), front-to-back (gamma) and &mdash; if the phone or laptop has a compass &mdash; the direction the device is facing (alpha).

Let’s see some examples:

[[Image:up03.jpg]]<br/>
''You’re looking north, while the device is on a flat surface, facing north''<br/>
<code>{evt.alpha: 0, evt.beta: 0, evt.gamma: 0}</code>

[[Image:up04.png]]<br/>
''You’re looking north, while the device is on a flat surface, pointed south''<br/>
<code>{evt.alpha: 180, evt.beta: 0, evt.gamma: 0}</code>

[[Image:up05.jpg]]<br/>
''The device is leaning to the right, facing north, but doesn’t have a compass''<br/>
<code>{evt.alpha: null, evt.beta: 0, evt.gamma: 45}</code>

[[Image:up06.jpg]]<br/>
''The device is leaning toward the user, facing north''<br/>
<code>{evt.alpha: 0, evt.beta: 45, evt.gamma: 0}</code>

===MozOrientation===

Firefox has a slightly different implementation of the device orientation event, and instead uses the [https://developer.mozilla.org/en/Detecting_device_orientation#Processing_orientation_events MozOrientationEvent]. The MozOrientationEvent provides information about the side-to-side tilt (using the parameter x), the front-to-back tilt (using the parameter y), and, instead of providing the compass direction, it provides the vertical acceleration (using the parameter z).

The <code>MozOrientation</code> event returns three values:

* <code>X</code> - the amount of side-to-side tilt. When the laptop or phone is level, the value is zero; it approaches +1 when tilted to the left and approaches -1 when tilted to the right.
* <code>Y</code> - the amount of front-to-back tilt. When the laptop is level, the value is zero; it approaches +1 as it’s titled away from you and approaches -1 as it’s tilted toward you.
* <code>Z</code> - the amount of vertical acceleration. When undergoing normal earth gravity the value is -1; it decreases as the device is moved up. The value is 0 if the device is thrust up.

===Device motion===

The device motion event is a superset of the device orientation event; it returns data about the rotation information and also [http://en.wikipedia.org/wiki/Acceleration acceleration] information about the device. The acceleration data is returned in three axes: x, y, and z. The axes are measured in meters per second per second, or [http://en.wikipedia.org/wiki/Metre_per_second_per_second meters per second squared] (m/s^2). Because some devices might not have the hardware to exclude the effect of gravity, the event returns two properties, <code>accelerationIncludingGravity</code> and <code>acceleration</code>, which excludes the effects of gravity. (When this is the case, the acceleration data will be null).

For a laptop in its normal position, with the screen facing up, the data returned would be:<br/>

{{{!}}
! 
! Not accelerating
! Accelerating up
! Accelerating forward
! Accelerating left
! Accelerating up and to the right
{{!}}-
{{!}} ''acceleration''
{{!}} {0, 0, 0}
{{!}} {0, 0, 5}
{{!}} {0, 2, 0}
{{!}} {3, 0, 0}
{{!}} {5, 0, 9}
{{!}}-
{{!}} ''accelerationIncludingGravity''
{{!}} {0, 0, 9.81}
{{!}} {0, 0, 15}
{{!}} {0, 2, 9.81}
{{!}} {3, 0, 9.81}
{{!}} {5, 0, 11}
{{!}}}

A mobile phone rotated along the x-axis so the screen is perpendicular to its normal position would return:

{{{!}}
! 
! Not accelerating
! Accelerating up
! Accelerating forward
! Accelerating left
! Accelerating up and to the right
{{!}}-
{{!}} ''acceleration''
{{!}} {0, 0, 0}
{{!}} {0, 5, 0}
{{!}} {0, 0, 2}
{{!}} {3, 0, 0}
{{!}} {5, 5, 0}
{{!}}-
{{!}} ''accelerationIncludingGravity''
{{!}} {0, 9.81, 0}
{{!}} {0, 15, 0}
{{!}} {0, 9.81, 2}
{{!}} {3, 9.81, 0}
{{!}} {5, 11, 0}
{{!}}}

==Using the DeviceOrientation events==

Since DeviceOrientation and MozOrientation are similar, we’ll look at them together in this sample.

===1. Check for compatibility===

Check to see if either the DeviceOrientationEvent or the MozOrientationEvent is supported.
 
 if (window.DeviceOrientationEvent) {
  console.log("DeviceOrientation is supported");
 } else if (window.OrientationEvent) {
  console.log("MozOrientation is supported");
 }

One thing to note: some devices (for example, the original iPad) say that they support the event when in fact they don’t. In these cases, the event is fired only once, and all of the properties are null.

===2. Declare the markup===

For this example, we’re going to display the orientation data and then apply that information as a CSS3 transform to an image.
 
 &lt;div class="main"&gt;
   &lt;h2&gt;Device Orientation&lt;/h2&gt;
   &lt;table&gt;
     &lt;tr&gt;
       &lt;td&gt;Event Supported&lt;/td&gt;
       &lt;td id="doEvent"&gt;&lt;/td&gt;
     &lt;/tr&gt;
     &lt;tr&gt;
       &lt;td&gt;Tilt Left/Right [tiltLR]&lt;/td&gt;
       &lt;td id="doTiltLR"&gt;&lt;/td&gt;
     &lt;/tr&gt;
     &lt;tr&gt;
       &lt;td&gt;Tilt Front/Back [tiltFB]&lt;/td&gt;
       &lt;td id="doTiltFB"&gt;&lt;/td&gt;
     &lt;/tr&gt;
     &lt;tr&gt;
       &lt;td&gt;Direction [direction]&lt;/td&gt;
       &lt;td id="doDirection"&gt;&lt;/td&gt;
     &lt;/tr&gt;
     &lt;tr&gt;
       &lt;td&gt;Motion Up/Down&lt;/td&gt;
       &lt;td id="doMotionUD"&gt;&lt;/td&gt;
     &lt;/tr&gt;
    &lt;/table&gt;
 &lt;/div&gt;
 
 &lt;div class="container" style="-webkit-perspective: 300; perspective: 300;"&gt;
   &lt;img src="html5_logo.png" id="imgLogo" class="logo"&gt;
 &lt;/div&gt;

===3. Add an event listener===

Now that we know what events are supported, add the appropriate event listeners:
 
 if (window.DeviceOrientationEvent) {
   // Listen for the deviceorientation event and handle DeviceOrientationEvent object
   window.addEventListener('deviceorientation', devOrientHandler, false);
 } else if (window.OrientationEvent) {
   // Listen for the MozOrientation event and handle OrientationData object
   window.addEventListener('MozOrientation', mozDevOrientHandler, false);
 }

===4. Normalize the data===

The HTML5 DeviceOrientation event returns three pieces of data:

* <code>alpha</code> the direction the device is facing according to the compass
* <code>beta</code> the angle in degrees the device is tilted front-to-back
* <code>gamma</code> the angle in degrees the device is tilted left-to-right.

 The angles values increase as you tilt the device to the right or toward you.

Since Firefox uses the <code>MozOrientationEvent</code> which returns similar data but using different parameters and a different measurement system, we want to normalize that before we pass it to our <code>deviceOrientationHandler</code> function.
 
 if (window.DeviceOrientationEvent) {
   document.getElementById("doEvent").innerHTML = "DeviceOrientation";
   // Listen for the deviceorientation event and handle the raw data
   window.addEventListener('deviceorientation', function(eventData) {
     // gamma is the left-to-right tilt in degrees, where right is positive
     var tiltLR = eventData.gamma;
 
     // beta is the front-to-back tilt in degrees, where front is positive
     var tiltFB = eventData.beta;
 
     // alpha is the compass direction the device is facing in degrees
     var dir = eventData.alpha
 
     // deviceorientation does not provide this data
     var motUD = null;
 
     // call our orientation event handler
     deviceOrientationHandler(tiltLR, tiltFB, dir, motUD);
   }, false);
 } else if (window.OrientationEvent) {
   document.getElementById("doEvent").innerHTML = "MozOrientation";
   window.addEventListener('MozOrientation', function(eventData) {
     // x is the left-to-right tilt from -1 to +1, so we need to convert to degrees
     var tiltLR = eventData.x * 90;
 
     // y is the front-to-back tilt from -1 to +1, so we need to convert to degrees
     // We also need to invert the value so tilting the device towards us (forward) 
     // results in a positive value. 
     var tiltFB = eventData.y * -90;
 
     // MozOrientation does not provide this data
     var dir = null;
 
     // z is the vertical acceleration of the device
     var motUD = eventData.z;
     
     // call our orientation event handler
     deviceOrientationHandler(tiltLR, tiltFB, dir, motUD);
   }, false);
 } else {
   document.getElementById("doEvent").innerHTML = "Not supported on your device or browser."
 }

===5. Create an event handler===

We’ve already normalized our data, so we’ll display it in the table we created in step 2, and also rotate the image using a CSS3 transform.
 
 document.getElementById("doTiltLR").innerHTML = Math.round(tiltLR);
 document.getElementById("doTiltFB").innerHTML = Math.round(tiltFB);
 document.getElementById("doDirection").innerHTML = Math.round(dir);
 document.getElementById("doMotionUD").innerHTML = motionUD;
 
 // Apply the transform to the image
 document.getElementById("imgLogo").style.webkitTransform = "rotate(" + 
   tiltLR + "deg) rotate3d(1,0,0, " + (tiltFB * -1) + "deg)";
 document.getElementById("imgLogo").style.MozTransform = "rotate(" + tiltLR + "deg)";
 document.getElementById("imgLogo").style.transform = "rotate(" + tiltLR + 
   "deg) rotate3d(1,0,0, " + (tiltFB * -1) + "deg)";

===The final product===

[[Image:up07.png]]

Try it out [http://www.html5rocks.com/en/tutorials/device/orientation/deviceorientationsample.html here], and view the source to see it in action.

==Using the DeviceMotion events==

The <code>DeviceMotionEvent</code> provides the acceleration and rotation data of the device. In our example, we’re going to use <code>accelerationIncludingGravity</code> to determine the orientation of the device and get a similar result to the sample we built with <code>DeviceOrientation</code>.

===1. Check for compatibility===

First thing we want to do is determine if the DeviceMotionEvent is supported using feature detection.
 
 if (window.DeviceMotionEvent) {
   console.log("DeviceMotionEvent supported");
 } 

Like <code>DeviceOrientationEvent</code>, if a browser cannot provide motion information, the event will be fired once and all properties will be null.

===2. Add an event listener===

Now that we know that the browser and device supports the DeviceMotionEvent, we can add an event listener.
 
 if ((window.DeviceMotionEvent) {
   window.addEventListener('devicemotion', deviceMotionHandler, false);
 } else {
   document.getElementById("dmEvent").innerHTML = "Not supported on your device."
 }

===3. Declare the markup===

For this example, we’re just going to display data that we receive.
 
 &lt;div class="main"&gt;
   &lt;h2&gt;Device Motion&lt;/h2&gt;
   &lt;table&gt;
     &lt;tr&gt;
       &lt;td&gt;Event Supported&lt;/td&gt;
       &lt;td id="dmEvent"&gt;&lt;/td&gt;
     &lt;/tr&gt;
     &lt;tr&gt;
       &lt;td&gt;accelerationIncludingGravity&lt;/td&gt;
       &lt;td id="moAccel"&gt;&lt;/td&gt;
     &lt;/tr&gt;
     &lt;tr&gt;
       &lt;td&gt;Calculated Left-Right Tilt&lt;/td&gt;
       &lt;td id="moCalcTiltLR"&gt;&lt;/td&gt;
     &lt;/tr&gt;
     &lt;tr&gt;
       &lt;td&gt;Calculated Front-Back Tilt&lt;/td&gt;
       &lt;td id="moCalcTiltFB"&gt;&lt;/td&gt;
     &lt;/tr&gt;
   &lt;/table&gt;
 &lt;/div&gt;
 
 &lt;div class="container" style="-webkit-perspective: 300; perspective: 300;"&gt;
   &lt;img src="html5_logo.png" id="imgLogo" class="logo"&gt;
 &lt;/div&gt;

===4. Create an event handler===

We want to display the raw data that we get back, but also convert that into something that we can use to rotate our image, so we need to do a little math to convert from m/s^2 to an angle.
 
 function deviceMotionHandler(eventData) {
   // Grab the acceleration including gravity from the results
   var acceleration = eventData.accelerationIncludingGravity;
 
   // Display the raw acceleration data
   var rawAcceleration = "[" +  Math.round(acceleration.x) + ", " + 
     Math.round(acceleration.y) + ", " + Math.round(acceleration.z) + "]";
 
   // Z is the acceleration in the Z axis, and if the device is facing up or down
   var facingUp = -1;
   if (acceleration.z &gt; 0) {
     facingUp = +1;
   }
   
   // Convert the value from acceleration to degrees acceleration.x{{!}}y is the 
   // acceleration according to gravity, we'll assume we're on Earth and divide 
   // by 9.81 (earth gravity) to get a percentage value, and then multiply that 
   // by 90 to convert to degrees.                                
   var tiltLR = Math.round(((acceleration.x) / 9.81) * -90);
   var tiltFB = Math.round(((acceleration.y + 9.81) / 9.81) * 90 * facingUp);
 
   // Display the acceleration and calculated values
   document.getElementById("moAccel").innerHTML = rawAcceleration;
   document.getElementById("moCalcTiltLR").innerHTML = tiltLR;
   document.getElementById("moCalcTiltFB").innerHTML = tiltFB;
 
   // Apply the 2D rotation and 3D rotation to the image
   var rotation = "rotate(" + tiltLR + "deg) rotate3d(1,0,0, " + (tiltFB) + "deg)";
   document.getElementById("imgLogo").style.webkitTransform = rotation;        
 }

===The final product===

When you load the page and move the device around the bottom of the HTML5 logo should always point down, towards earth.

[[Image:up08.jpg]]

Try it out [http://www.html5rocks.com/en/tutorials/device/orientation/devicemotionsample.html here], and view the source to see it in action.

==Additional resources==

Here are a few other resources and demos you can check out that use the HTML5 device orientation or device motion events.

===Physics articles===

* [http://en.wikipedia.org/wiki/Acceleration Acceleration]
* [http://en.wikipedia.org/wiki/Acceleration_of_gravity Acceleration of Gravity]
* [http://en.wikipedia.org/wiki/Acceleration_of_gravity#Earth.27s_gravity Acceleration of Gravity on Earth]
* [http://en.wikipedia.org/wiki/Euler_angles Euler Angles]

===The Specs===

* [http://dev.w3.org/geo/api/spec-source-orientation W3C Device Orientation Event Specification]
* [https://developer.mozilla.org/en/XPCOM_Interface_Reference/nsIDOMOrientationEvent Mozilla DOM Orientation Event]
* [https://developer.mozilla.org/en/Detecting_device_orientation#Processing_orientation_events Mozilla Processing Orientation Events]

===A neat demo===

[http://petelepage.com/scratch/pong/ Pong] An experiment to try out device orientation in gaming.

}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Device orientation events
|Chrome_supported=Yes
|Chrome_version=21.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=14.0 (partial)
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
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
|Feature=Device orientation events
|Android_supported=Yes
|Android_version=3.0
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
|Safari_mobile_version=4.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Mobile}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=http://www.html5rocks.com/en/tutorials/device/orientation/
}}