{{Page_Title|Pointer Events Primer}}
{{Flags}}
{{API_Name}}
{{Summary_Section|This document is written for web developers who have basic familiarity with [http://docs.webplatform.org/wiki/html HTML] and [http://docs.webplatform.org/wiki/javascript JavaScript].  This document should help you:
# Understand the end-user and web developer problems that Pointer Events address
# Easily add Pointer Events to an existing web page
# Take advantage of additional methods and attributes available in Pointer Events
# Find additional resources to learn more about Pointer Events
}}
{{Concept_Page
|Content=__TOC__

==1. WHY POINTER EVENTS==

===1.1 UNIFIED MODEL FOR MULTIPLE INPUT TYPES===
In the last few years, there has been an explosion of computing devices that use mechanisms other than a mouse for end user input.  These input mechanisms include touch as on a smartphone or pen/stylus as on a slate.  All of today’s web browsers support mouse events (mouseover, mousedown, mousemove, etc.) but many users aren’t using a mouse.  Today’s user may be interacting with a web page using their fingers on a smartphone while riding public transit or using a pen on a slate/tablet while in a meeting.  Pointer Events provides a unified model for all three of these input types without requiring web developers to write unique code for each.  And Pointer Events is intended to be forward compatible covering future interaction paradigms.

===1.2 ABILITY TO IDENTIFY DIFFERENT INPUT TYPES===
Most modern browsers such as the latest versions of Chrome, Firefox, Internet Explorer, Opera, and Safari all map touch or pen input to mouse events.  But this makes it hard to know if a mouse event is an actual mouse event or was synthetically generated from a touch or pen input event.  Pointer Events also includes attributes to identify which mouse or pen button(s) were pressed during the event.  

===1.3 ADDITIONAL METHODS AND ATTRIBUTES===
Finally, Pointer Events provides additional attributes such as touch contact geometry size, pressure, and pen tilt so that web developers can take advantage of these additional inputs in building experiences for end users.  And if web developers want, they can write unique code for each input type.


==2. BASIC POINTER EVENTS==
Pointer Events includes a number of basic events similar to mouse events:


===2.1 DOWN AND UP (WITH EXAMPLE)===
Pointer Events includes basic pointer down and pointer up events.  
* <code>pointerdown</code> is triggered when a user clicks a mouse button or touches the screen with a finger or pen.
* <code>pointerup</code> is triggered when a user releases a mouse button or releases their finger or pen from touching the screen. 
The below example shows how pointerdown and pointerup are similar to mousedown and mouseup:

<syntaxhighlight lang="html5">
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title></title>
    <script type="text/javascript">
</syntaxhighlight>
<syntaxhighlight lang="javascript">
        function MouseDownResponse(event) {
            document.getElementById("dvMouseStatus").innerHTML += "Mouse Down<br />";
        }

        function MouseUpResponse(event) {
            document.getElementById("dvMouseStatus").innerHTML += "Mouse Up<br />";
        }

        function PointerDownResponse(event) {
            document.getElementById("dvPointerStatus").innerHTML +=
                "PointerId:" + event.pointerId +
                " of pointerType:" + event.pointerType + " Down<br />";
        }

        function PointerUpResponse(event) {
            document.getElementById("dvPointerStatus").innerHTML +=
                "PointerId:" + event.pointerId +
                " of pointerType:" + event.pointerType + " Up<br />";
        }

        function init() {
            document.addEventListener("mousedown", MouseDownResponse, false);
            document.addEventListener("mouseup", MouseUpResponse, false);

            document.addEventListener("pointerdown", PointerDownResponse, false);
            document.addEventListener("pointerup", PointerUpResponse, false);

            // Support for prefixed IE10 implementation
            document.addEventListener("MSPointerDown", PointerDownResponse, false);
            document.addEventListener("MSPointerUp", PointerUpResponse, false);
        }
</syntaxhighlight>
<syntaxhighlight lang="html5">
    </script>
</head>
<body onload="init()">
    <p>Click, touch, or tap</p>
    <table>
        <tr>
            <td style="vertical-align:top; width:30%;"><div id="dvMouseStatus"></div></td>
            <td style="vertical-align:top; width:40%;"><div id="dvPointerStatus"></div></td>
        </tr>
    </table>
</body>
</html>
</syntaxhighlight>


===2.2 MOVE (WITH EXAMPLE)===
Pointer Events also includes a basic move event.  The <code>pointermove</code> event is triggered when a user moves their mouse, finger, or pen.
Many devices with touch screens have default pan and zoom behaviors such as zooming for a double tap.  Web developers can disable these default behaviors with the <code>touch-action</code> CSS value of <code>none</code> as shown in the below example.  
The below example shows how <code>pointermove</code> is similar to <code>mousemove</code>:
<syntaxhighlight lang="html5">
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title></title>
    <script type="text/javascript">
</syntaxhighlight>
<syntaxhighlight lang="javascript">
        function MouseMoveResponse(event) {
            document.getElementById("dvMouseStatus").innerHTML =
                "Mouse position: " + event.clientX + ", " + event.clientY + "<br />";
        }

        function PointerMoveResponse(event) {
            document.getElementById("dvPointerStatus").innerHTML =
                "PointerId:" + event.pointerId + " of pointerType:" + event.pointerType +
                " isPrimary:" + event.isPrimary +
                " position: " + event.clientX + ", " + event.clientY + "<br />";
        }

        function init() {
            document.addEventListener("mousemove", MouseMoveResponse, false);
            document.addEventListener("pointermove", PointerMoveResponse, false);

            // Support for prefixed IE10 implementation
            document.addEventListener("MSPointerMove", PointerMoveResponse, false);
        }
</syntaxhighlight>
<syntaxhighlight lang="html5">
    </script>
</head>
<body onload="init()" style="touch-action:none; -ms-touch-action:none;">
    <p>Move your mouse, finger, or pen</p>
    <table>
        <tr>
            <td style="vertical-align:top; width:30%;"><div id="dvMouseStatus"></div></td>
            <td style="vertical-align:top; width:40%;"><div id="dvPointerStatus"></div></td>
        </tr>
    </table>
</body>
</html>
</syntaxhighlight>
In addition to the basic x and y coordinates, <code>pointermove</code> includes <code>pointerId</code>, <code>pointerType</code>, and other attributes.


===2.3 OVER AND OUT (WITH EXAMPLE)===
Pointer Events includes basic pointer over and pointer out events.  
* <code>pointerover</code> is triggered when a user moves their mouse over an HTML element or touches it with their finger or pen. 
* <code>pointerout</code> is triggered when a user moves their mouse out of an HTML element, releases a finger or pen touch, or moves their finger our out of an HTML element while still touching the screen.
The below example shows how <code>pointerover</code> and <code>pointerout</code> are similar to <code>mouseover</code> and <code>mouseout</code>.
<syntaxhighlight lang="html5">
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title></title>
    <script type="text/javascript">
</syntaxhighlight>
<syntaxhighlight lang="javascript">
        function MouseOverResponse(event) {
            document.getElementById("dvMouseStatus").innerHTML += "Mouse Over<br />";
        }

        function MouseOutResponse(event) {
            document.getElementById("dvMouseStatus").innerHTML += "Mouse Out<br />";
        }

        function PointerOverResponse(event) {
            document.getElementById("dvPointerStatus").innerHTML += "Pointer Over<br />";
        }

        function PointerOutResponse(event) {
            document.getElementById("dvPointerStatus").innerHTML += "Pointer Out<br />";
        }

        function init() {
            var dvObject = document.getElementById("dvObject");

            dvObject.addEventListener("mouseover", MouseOverResponse, false);
            dvObject.addEventListener("mouseout", MouseOutResponse, false);

            dvObject.addEventListener("pointerover", PointerOverResponse, false);
            dvObject.addEventListener("pointerout", PointerOutResponse, false);

            // Support for prefixed IE10 implementation
            dvObject.addEventListener("MSPointerOver", PointerOverResponse, false);
            dvObject.addEventListener("MSPointerOut", PointerOutResponse, false);
        }
</syntaxhighlight>
<syntaxhighlight lang="html5">
    </script>
</head>
<body onload="init()">
    <p>Move your mouse, finger, or pen/stylus over the yellow box</p>
    <div id="dvObject" style="float:right; background-color:yellow; height:100px; width:200px;">
    </div>
    <table>
        <tr>
            <td style="vertical-align:top; width:30%;"><div id="dvMouseStatus"></div></td>
            <td style="vertical-align:top; width:40%;"><div id="dvPointerStatus"></div></td>
        </tr>
    </table>
</body>
</html>
</syntaxhighlight>


===2.4 ENTER AND LEAVE (WITH EXAMPLE)===
Pointer Events includes basic pointer enter and pointer leave events.  Enter and leave events are similar to over and out events described in the previous section but with some exceptions including that they do not bubble.  
* <code>pointerenter</code> is triggered when a user moves their mouse over an HTML element or touches it with their finger or pen.
* <code>pointerleave</code> is triggered when a user moves their mouse out of an HTML element, releases a finger or pen touch, or moves their finger our out of an HTML element while still touching the screen.
The below example shows how <code>pointerenter</code> and <code>pointerleave</code> are similar to <code>mouseenter</code> and <code>mouseleave</code>.
<syntaxhighlight lang="html5">
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title></title>
    <script type="text/javascript">
</syntaxhighlight>
<syntaxhighlight lang="javascript">
        function MouseEnterResponse(event) {
            document.getElementById("dvMouseStatus").innerHTML += "Mouse Enter<br />";
        }

        function MouseLeaveResponse(event) {
            document.getElementById("dvMouseStatus").innerHTML += "Mouse Leave<br />";
        }

        function PointerEnterResponse(event) {
            document.getElementById("dvPointerStatus").innerHTML += "Pointer Enter<br />";
        }

        function PointerLeaveResponse(event) {
            document.getElementById("dvPointerStatus").innerHTML += "Pointer Leave<br />";
        }

        function init() {
            var dvObject = document.getElementById("dvObject");

            dvObject.addEventListener("mouseenter", MouseEnterResponse, false);
            dvObject.addEventListener("mouseleave", MouseLeaveResponse, false);

            dvObject.addEventListener("pointerenter", PointerEnterResponse, false);
            dvObject.addEventListener("pointerleave", PointerLeaveResponse, false);
        }
</syntaxhighlight>
<syntaxhighlight lang="html5">
    </script>
</head>
<body onload="init()">
    <p>Move your mouse, finger, or pen/stylus over the orange box</p>
    <div id="dvObject" style="float:right; background-color:orange; height:100px; width:200px;">
    </div>
    <table>
        <tr>
            <td style="vertical-align:top; width:30%;"><div id="dvMouseStatus"></div></td>
            <td style="vertical-align:top; width:40%;"><div id="dvPointerStatus"></div></td>
        </tr>
    </table>
</body>
</html>
</syntaxhighlight>


===2.5 CANCEL===
In the modern world of desktop PC’s with multiple monitors or smartphones and slates supporting multiple orientations, there are cases where a pointer is down and the next event should be a <code>pointercancel</code> event; rather than a <code>pointerup</code> event.  These include:
* A user changes the position of a screen in a multi-screen configuration
* A user changes the orientation of a screen (i.e. rotate from portrait to landscape)
* A user exceeds the number of simultaneous contacts a device can support
* A user locks their device or logs-off
In all of these cases, a <code>pointercancel</code> event is triggered.  This gives the developer a chance to handle any clean-up that is needed.  More information on <code>pointercancel</code> cases can be found at: http://msdn.microsoft.com/en-us/library/ie/hh846776(v=vs.85).aspx 


===2.6 COMPARISON OF MOUSE EVENTS AND POINTER EVENTS===
The below table lists Mouse Events and the related Pointer Events:
<table>
<tr><th>Mouse Event</th><th>Pointer Event</th><th>(Prefixed) IE10 Pointer Event</th></tr>
<tr><td>mousedown</td><td>pointerdown</td><td>MSPointerDown</td></tr>
<tr><td>mouseup</td><td>pointerup</td><td>MSPointerUp</td></tr>
<tr><td>mousemove</td><td>pointermove</td><td>MSPointerMove</td></tr>
<tr><td>mouseover</td><td>pointerover</td><td>MSPointerOver</td></tr>
<tr><td>mouseout</td><td>pointerout</td><td>MSPointerOut</td></tr>
<tr><td>mouseenter</td><td>pointerenter</td><td>(none)</td></tr>
<tr><td>mouseleave</td><td>pointerleave</td><td>(none)</td></tr>
<tr><td>(none)</td><td>pointercancel</td><td>MSPointerCancel</td></tr>
</table>


== 3 POINTER EVENT ATTRIBUTES==
Pointer Events have a number of additional attributes that enable you as a web developer to enhance your interactions:

===3.1 POINTERTYPE===
The <code>pointerType</code> attribute tells you if a pointer is a mouse, a touch, a pen, or some new future pointer type. Use of the <code>pointerType</code> attribute was shown in the earlier examples for <code>pointerdown</code>, <code>pointerup</code>, and <code>pointermove</code>.  As a best practice, if you are writing code that behaves uniquely for different <code>pointerType</code> values you should make sure to also handle a new future pointer type.  

===3.2 POINTERID===
The <code>pointerId</code> attribute tells you which pointer you’re interacting with.  The mouse always has a <code>pointerId</code> of 1, and touch and pen pointers have integer <code>pointerId</code> values that are not 1.  

===3.3 ISPRIMARY===
The <code>isPrimary</code> attribute tells you which pointer is the “primary” pointer for that device type:
* For mouse, there is only one pointer so it is primary for the mouse type
* For touch, a pointer is considered primary if the user touched the screen where there were no other active touches
* For pen, a pointer is considered primary if the user’s pen initially contacted the screen when there were no other active pens contacting the screen.
Two potential uses for the <code>isPrimary</code> attribute are:
* If you are intending to support only single touch (and not multi-touch) only react if the pointer <code>isPrimary</code>.
* If you want to see which pointer will also generate Mouse Events, check the <code>isPrimary</code> attribute.


=== 4.4 CONTACT GEOMETRY WIDTH AND HEIGHT===
With some input types (especially touch) and screens of increasing resolution, the contact area between the pointer and the screen can be more than a single pixel.  The <code>width</code> and <code>height</code> attributes indicate the width and height of the contact between the pointer and the screen.
The below example shows the width and height attributes:
<syntaxhighlight lang="html5">
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title></title>
    <script type="text/javascript">
</syntaxhighlight>
<syntaxhighlight lang="javascript">
        function PointerDownInfo(event) {
            document.getElementById("dvPointerStatus").innerHTML += 
                "Height:" + event.height + " Width:" + event.width + "<br />";
        }

        function init() {
            document.addEventListener("pointerdown", PointerDownInfo, false);

            // Support for legacy IE10 implementation
            document.addEventListener("MSPointerDown", PointerDownInfo, false);
        }
</syntaxhighlight>
<syntaxhighlight lang="html5">
    </script>
</head>
<body onload="init()">
    <p>Click, touch, or tap</p>
    <div id="dvPointerStatus"></div>
</body>
</html>
</syntaxhighlight>


===3.5 PRESSURE===
Another attribute that you can get with Pointer Events is <code>pressure</code>.  If the hardware supports it, <code>pressure</code> is a floating point value between 0 and 1 (inclusive) where 0 represents no force per area and 1 represents the maximum force per area that the hardware can detect.  If the hardware does not support detecting <code>pressure</code>, the browser might simulate values for pointer devices that do not report pressure such as 0.5 for any action.
 
===3.6 PEN TILTX AND TILTY===
Like <code>pressure</code>, if the hardware supports it, the tilt of the pen is also included on Pointer Events.  There are two measures:
* <code>tiltX</code> measures the angle in degrees (-90 to 90) between the pen and a plane formed by the Y Axis and Z Axis as shown below:
[[File:TiltX.png|alt=Image showing positive TiltX]]
* <code>tiltY</code> measures the angle in degrees (-90 to 90) between the pen and a plane formed by the X Axis and Z Axis as shown below:
[[File:TiltX.png|alt=Image showing positive TiltY]]

If the pen is perpendicular to the plane formed by the X Axis and Y Axis, then it’s <code>tiltX</code> and <code>tiltY</code> values will both be zero.

==4 MULTIPLE POINTERS AT ONCE / MULTI-TOUCH (WITH EXAMPLE)==
Pointer Events allows for interacting with multiple pointers at once.  However, there are some systems where two touches on a screen at once causes the screen to pan or zoom.  

As the developer, you can disable pan and zoom behaviors by setting the CSS style of <code>touch-action</code> to none.  For example:
<syntaxhighlight lang="html5">
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title></title>
    <script type="text/javascript">
</syntaxhighlight>
<syntaxhighlight lang="javascript">
        function PointerDownResponse(event) {
            document.getElementById("dvPointerStatus").innerHTML +=
                "PointerId:" + event.pointerId +
                " of pointerType:" + event.pointerType + " Down<br />";
        }

        function init() {
            document.addEventListener("pointerdown", PointerDownResponse, false);

            // Support for prefixed IE10 implementation
            document.addEventListener("MSPointerDown", PointerDownResponse, false);
        }
</syntaxhighlight>
<syntaxhighlight lang="html5">
    </script>
</head>
<body onload="init()">
    <p>Try touching within each box with multiple fingers</p>
    <div id="dvPointerStatus" style="float:left; width:200px;"></div>
    <div style="float:left; background-color:orange; height:300px; width:300px">
            Touches in this box will invoke default pan and zoom behaviors
    </div>
    <div style="float:left; background-color:blue; height:300px; width:300px; 
        touch-action:none; -ms-touch-action:none;">
            This box has touch-action set to none
    </div>
</body>
</html>
</syntaxhighlight>
By disabling pan and zoom behaviors, you can capture Pointer Events for multiple pointers at the same time and build exciting multi-touch interactive experiences for your end-users.


==5 DETECTING WHICH BUTTON(S) ARE PRESSED==
Another opportunity for building new interactive experiences for your end-users is multi-button interactions.

Pointer Events provides <code>button</code> and <code>buttons</code> that indicate which input device button(s) were involved in an interaction.  For example:
<syntaxhighlight lang="html5">
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title></title>
    <script type="text/javascript">
</syntaxhighlight>
<syntaxhighlight lang="javascript">
        function PointerDownInfo(event) {
            document.getElementById("dvPointerStatus").innerHTML += 
                "Button: " + event.button + " Buttons: " + event.buttons + "<br />";
        }

        function init() {
            document.addEventListener("pointerdown", PointerDownInfo, false);

            // Support for legacy IE10 implementation
            document.addEventListener("MSPointerDown", PointerDownInfo, false);
        }
</syntaxhighlight>
<syntaxhighlight lang="html5">
    </script>
</head>
<body onload="init()">
    <p>Click, touch, or tap</p>
    <div id="dvPointerStatus"></div>
</body>
</html>
</syntaxhighlight>

Below is the list of potential values for <code>button</code> and <code>buttons</code>:
<table>
<tr><th>Device Button State</th><th>button</th><th>buttons</th></tr>
<tr><td>Mouse move with no buttons pressed</td><td>-1</td><td>0</td></tr>
<tr><td>Left Mouse, Touch Contact, Pen contact (with no modifier buttons pressed)</td><td>0</td><td>1</td></tr>
<tr><td>Middle Mouse</td><td>1</td><td>4</td></tr>
<tr><td>Right Mouse, Pen contact with barrel button pressed</td><td>2</td><td>2</td></tr>
<tr><td>X1 (back) Mouse</td><td>3</td><td>8</td></tr>
<tr><td>X2 (forward) Mouse</td><td>4</td><td>16</td></tr>
<tr><td>Pen contact with eraser button pressed</td><td>5</td><td>32</td></tr>
</table>


==6 TRY POINTER EVENTS TODAY WITH IMPLEMENTATIONS==
You can tell if a browse supports Pointer Events by checking the <code>navigator.PointerEnabled</code> attribute:
<syntaxhighlight lang="html5">
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title></title>
    <script type="text/javascript">
</syntaxhighlight>
<syntaxhighlight lang="javascript">
        function init() {
            if ( (navigator.pointerEnabled) || (navigator.msPointerEnabled) ) {
                document.getElementById("dvPointerStatus").innerHTML = 
                    "This browser supports Pointer Events :)<br />and supports " +
                    navigator.maxTouchPoints + " simultaneous touch contacts.";
            } else {
                document.getElementById("dvPointerStatus").innerHTML = 
                    "This browser does not support Pointer Events. :("
            }
        }
</syntaxhighlight>
<syntaxhighlight lang="html5">
    </script>
</head>
<body onload="init()">
    <p>Checking your browser...</p>
    <div id="dvPointerStatus"></div>
</body>
</html>
</syntaxhighlight>
Also shown in the above example is how to use the <code>navigator.maxTouchPoints</code> attribute to check the maximum number of touch points the hardware supports.


===6.1 WEBKIT WITH POINTER EVENTS PATCH===
As of February 2013, builds of WebKit with the Pointer Events patch for OSX and Windows are linked from this blog post by appendTo: http://appendto.com/blog/2013/02/prototype-chromium-build-with-support-for-ms-pointer-events/


===6.2 INTERNET EXPLORER 10===
A version of Pointer Events was implemented in IE10 and Pointer Events are prefixed with “MS” (for Microsoft.)

IE10 is included with Windows 8 and Windows Server 2012.  

IE10 for Windows 7 or Windows Server 2008 can be downloaded from: 
http://windows.microsoft.com/en-US/internet-explorer/downloads/ie-10/worldwide-languages


==7 FURTHER READING==
If you’re interested in the W3C standardization process for Pointer Events, here are some useful links:
* Specification: http://www.w3.org/TR/pointerevents/ 
* Working Group: http://www.w3.org/2012/pointerevents/ 
* Working Group Charter: http://www.w3.org/2012/pointerevents/charter/ 
* Working Group Listserv: mailto:public-pointer-events@w3.org 
* Working Group Listserv Archive: http://lists.w3.org/Archives/Public/public-pointer-events/ 

If you’re interested in the patch that adds Pointer Events to WebKit, see:
* 2013-02-11 (AppendTo Blog): [http://appendto.com/blog/2013/02/prototype-chromium-build-with-support-for-ms-pointer-events/ Prototype Chromium build with support for MS Pointer Events]
* 2012-12-18 (Interoperability @ Microsoft): [http://blogs.msdn.com/b/interoperability/archive/2012/12/18/open-source-release-from-ms-open-tech-pointer-events-initial-prototype-for-webkit.aspx Open source release from MS Open Tech: Pointer Events initial prototype for WebKit]
* 2012-12-18 (HTML5 Labs): [http://html5labs.interoperabilitybridges.com/prototypes/pointer-events-for-webkit/pointer-events-for-webkit/info Pointer Events for WebKit]

If you’re interested in some of the history and evolution of Pointer Events, visit these links from the IEBlog:
* 2012-11-12 (IEBlog): [http://blogs.msdn.com/b/ie/archive/2012/11/12/w3c-charters-pointer-events-working-group.aspx W3C Charters Pointer Events Working Group]
* 2012-09-24 (IEBlog): [http://blogs.msdn.com/b/ie/archive/2012/09/24/towards-interoperable-pointer-events-evolving-input-events-for-multiple-devices.aspx Towards Interoperable Pointer Events: Evolving Input Events for Multiple Devices]
* 2012-04-20 (IEBlog): [http://blogs.msdn.com/b/ie/archive/2012/04/20/guidelines-for-building-touch-friendly-sites.aspx Guildelines for Building Touch-friendly Sites]
* 2011-09-20 (IEBlog): [http://blogs.msdn.com/b/ie/archive/2011/09/20/touch-input-for-ie10-and-metro-style-apps.aspx Touch Input for IE10 and Metro style Apps]

Here are a few news articles about Pointer Events:
* 2012-12-20 (NeoWin): http://www.neowin.net/news/microsoft-offers-pointer-events-specs-to-webkit-developers 
* 2012-12-19 (Ars Technica): http://arstechnica.com/information-technology/2012/12/microsoft-offers-patches-to-webkit-to-aid-touch-compatibility/
* 2012-09-24 (The Next Web): http://thenextweb.com/microsoft/2012/09/24/the-w3c-accepted-published-microsofts-pointer-events-submission/
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Pointer Events
|URL=http://www.w3.org/TR/pointerevents/
|Status=Working Draft
}}
}}
{{See_Also_Section}}
{{Topics|DOM, DOMEvents, Touch}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}