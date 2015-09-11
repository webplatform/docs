---
title: Pointer Events Primer
notes:
  - dag
readiness: 'Almost Ready'
summary: "This document is written for web developers who have basic familiarity with HTML and JavaScript.  This document should help you:\n"
tags:
  - Concept
  - Pages
  - DOM
  - DOMEvents
  - Touch
uri: 'concepts/Pointer Events'

---
## <span>Summary</span>

This document is written for web developers who have basic familiarity with HTML and JavaScript. This document should help you:

1.  Understand the end-user and web developer problems that Pointer Events address
2.  Easily add Pointer Events to an existing web page
3.  Take advantage of additional methods and attributes available in Pointer Events
4.  Find additional resources to learn more about Pointer Events

## <span>Why Pointer Events?</span>

### <span>Unified Model for Multiple Input Types</span>

In the last few years, there has been an explosion of computing devices that use mechanisms other than a mouse for user input. These input mechanisms include touch as on a smartphone, or pen/stylus as on a slate. All of today's web browsers support mouse events (mouseover, mousedown, mousemove, etc.) but many users aren't using a mouse. Today's user may be interacting with a web page using their fingers on a smartphone while riding public transit, or using a pen on a slate/tablet while in a meeting. Pointer Events provides a unified model for all three of these input types without requiring web developers to write unique code for each. And Pointer Events is intended to be forward-compatible, covering future interaction paradigms.

### <span>Ability to Identify Different Input Types</span>

Most modern browsers such as Chrome, Firefox, Internet Explorer, Opera, and Safari all map touch or pen input to mouse events. But this makes it hard to know if a mouse event is an actual mouse event or if was synthetically generated from a touch or pen input event. Pointer Events also includes attributes to identify which mouse or pen button(s) were pressed during the event.

### <span>Additional Methods and Attributes</span>

Finally, Pointer Events provides additional attributes such as touch contact geometry size, pressure, and pen tilt so that web developers can take advantage of these additional inputs in building experiences for end users. And if web developers want, they can write unique code for each input type.

## <span>Basic Pointer Events</span>

Pointer Events includes a number of basic events similar to mouse events:

### <span>Down and Up</span>

Pointer Events includes basic pointer down and pointer up events.

-   `pointerdown` is triggered when a user clicks a mouse button or touches the screen with a finger or pen.
-   `pointerup` is triggered when a user releases a mouse button or releases their finger or pen from touching the screen.

The example below shows how pointerdown and pointerup are similar to mousedown and mouseup:

``` html
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title></title>
    <script type="text/javascript">
```

``` js
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
```

``` html
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
```

### <span>Move</span>

Pointer Events also includes a basic move event. The `pointermove` event is triggered when a user moves their mouse, finger, or pen. Many devices with touch screens have default pan and zoom behaviors, such as zooming for a double tap. Web developers can disable these default behaviors with the `touch-action` CSS value of `none` as shown below. This example shows how `pointermove` is similar to `mousemove`:

``` html
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title></title>
    <script type="text/javascript">
```

``` js
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
```

``` html
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
```

In addition to the basic x and y coordinates, `pointermove` includes `pointerId`, `pointerType`, and other attributes.

### <span>Over and Out</span>

Pointer Events includes basic pointer over and pointer out events.

-   `pointerover` is triggered when a user moves their mouse over an HTML element or touches it with their finger or pen.
-   `pointerout` is triggered when a user moves their mouse out of an HTML element, releases a finger or pen touch, or moves their finger our out of an HTML element while still touching the screen.

This example shows how `pointerover` and `pointerout` are similar to `mouseover` and `mouseout`.

``` html
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title></title>
    <script type="text/javascript">
```

``` js
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
```

``` html
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
```

### <span>Enter and Leave</span>

Pointer Events includes basic pointer enter and pointer leave events. Enter and leave events are similar to over and out events described in the previous section, but with some exceptions, including that they do not bubble.

-   `pointerenter` is triggered when a user moves their mouse over an HTML element or touches it with their finger or pen.
-   `pointerleave` is triggered when a user moves their mouse out of an HTML element, releases a finger or pen touch, or moves their finger our out of an HTML element while still touching the screen.

This example shows how `pointerenter` and `pointerleave` are similar to `mouseenter` and `mouseleave`.

``` html
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title></title>
    <script type="text/javascript">
```

``` js
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
```

``` html
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
```

### <span>Cancel</span>

In the modern world of desktop PCs with multiple monitors or smartphones and tablets supporting multiple orientations, there are cases where a pointer is down and the next event should be a `pointercancel` event; rather than a `pointerup` event. These include:

-   A user changes the position of a screen in a multi-screen configuration
-   A user changes the orientation of a screen (i.e. rotate from portrait to landscape)
-   A user exceeds the number of simultaneous contacts a device can support
-   A user locks their device or logs off

In all of these cases, a `pointercancel` event is triggered. This gives the developer a chance to handle any clean-up that is needed. More information on `pointercancel` cases can be found at: <http://msdn.microsoft.com/en-us/library/ie/hh846776(v=vs.85).aspx>

### <span>Comparison Of Mouse Events and Pointer Events</span>

The below table lists Mouse Events and the related Pointer Events:

|Mouse Event|Pointer Event|(Prefixed) IE10 Pointer Event|
|:----------|:------------|:----------------------------|
|mousedown|pointerdown|MSPointerDown|
|mouseup|pointerup|MSPointerUp|
|mousemove|pointermove|MSPointerMove|
|mouseover|pointerover|MSPointerOver|
|mouseout|pointerout|MSPointerOut|
|mouseenter|pointerenter|(none)|
|mouseleave|pointerleave|(none)|
|(none)|pointercancel|MSPointerCancel|

## <span>Pointer Event Attributes</span>

Pointer Events have a number of additional attributes that enable you, as a web developer, to enhance your interactions:

### <span>pointerType</span>

The `pointerType` attribute tells you if a pointer is a mouse, a touch, a pen, or some new future pointer type. Use of the `pointerType` attribute was shown in the earlier examples for `pointerdown`, `pointerup`, and `pointermove`. As a best practice, if you are writing code that behaves uniquely for different `pointerType` values you should make sure to also handle a new future pointer type.

### <span>pointerId</span>

The `pointerId` attribute tells you which pointer you're interacting with. The mouse always has a `pointerId` of 1, and touch and pen pointers have integer `pointerId` values that are not 1.

### <span>isPrimary</span>

The `isPrimary` attribute tells you which pointer is the *primary* pointer for that device type:

-   For mouse, there is only one pointer so it is primary for the mouse type
-   For touch, a pointer is considered primary if the user touched the screen where there were no other active touches
-   For pen, a pointer is considered primary if the user's pen initially contacted the screen when there were no other active pens contacting the screen

Two potential uses for the `isPrimary` attribute are:

-   If you are intending to support only single touch (and not multi-touch) only react if the pointer `isPrimary`
-   If you want to see which pointer will also generate Mouse Events, check the `isPrimary` attribute

### <span>Contact Geometry Width and Height</span>

With some input types (especially touch) and screens of increasing resolution, the contact area between the pointer and the screen can be more than a single pixel. The `width` and `height` attributes indicate the width and height of the contact between the pointer and the screen. The example below shows the width and height attributes:

``` html
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title></title>
    <script type="text/javascript">
```

``` js
        function PointerDownInfo(event) {
            document.getElementById("dvPointerStatus").innerHTML +=
                "Height:" + event.height + " Width:" + event.width + "<br />";
        }

        function init() {
            document.addEventListener("pointerdown", PointerDownInfo, false);

            // Support for legacy IE10 implementation
            document.addEventListener("MSPointerDown", PointerDownInfo, false);
        }
```

``` html
    </script>
</head>
<body onload="init()">
    <p>Click, touch, or tap</p>
    <div id="dvPointerStatus"></div>
</body>
</html>
```

### <span>pressure</span>

Another attribute that you can get with Pointer Events is `pressure`. If the hardware supports it, `pressure` is a floating point value between 0 and 1 (inclusive) where 0 represents no force per area and 1 represents the maximum force per area that the hardware can detect. If the hardware does not support detecting `pressure`, the browser might simulate values for pointer devices that do not report pressure, such as 0.5 for any action.

### <span>Pen tiltX and tiltY</span>

Like `pressure`, if the hardware supports it, the tilt of the pen is also included on Pointer Events. There are two measures:

-   `tiltX` measures the angle in degrees (-90 to 90) between the pen and a plane formed by the Y Axis and Z Axis as shown below:

![Image showing positive TiltX](/assets/public/2/20/TiltX.png)

-   `tiltY` measures the angle in degrees (-90 to 90) between the pen and a plane formed by the X Axis and Z Axis as shown below:

![Image showing positive TiltY](/assets/public/6/62/TiltY.png)

If the pen is perpendicular to the plane formed by the X Axis and Y Axis, then its `tiltX` and `tiltY` values will both be zero.

## <span>Multiple Pointers At Once / Multi-Touch</span>

Pointer Events allows for interacting with multiple pointers at once. However, there are some systems where two touches on a screen at once causes the screen to pan or zoom.

As the developer, you can disable pan and zoom behaviors by setting the CSS style of `touch-action` to none. For example:

``` html
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title></title>
    <script type="text/javascript">
```

``` js
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
```

``` html
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
```

 By disabling pan and zoom behaviors, you can capture Pointer Events for multiple pointers at the same time and build exciting multi-touch interactive experiences for your end-users.

## <span>Detecting which Button(s) are Pressed</span>

Another opportunity for building new interactive experiences for your end-users is multi-button interactions.

Pointer Events provides `button` and `buttons` that indicate which input device button(s) were involved in an interaction. For example:

``` html
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title></title>
    <script type="text/javascript">
```

``` js
        function PointerDownInfo(event) {
            document.getElementById("dvPointerStatus").innerHTML +=
                "Button: " + event.button + " Buttons: " + event.buttons + "<br />";
        }

        function init() {
            document.addEventListener("pointerdown", PointerDownInfo, false);

            // Support for legacy IE10 implementation
            document.addEventListener("MSPointerDown", PointerDownInfo, false);
        }
```

``` html
    </script>
</head>
<body onload="init()">
    <p>Click, touch, or tap</p>
    <div id="dvPointerStatus"></div>
</body>
</html>
```

 Here is the list of potential values for `button` and `buttons`:

|Device Button State|button|buttons|
|:------------------|:-----|:------|
|Mouse move with no buttons pressed|-1|0|
|Left Mouse, Touch Contact, Pen contact (with no modifier buttons pressed)|0|1|
|Middle Mouse|1|4|
|Right Mouse, Pen contact with barrel button pressed|2|2|
|X1 (back) Mouse|3|8|
|X2 (forward) Mouse|4|16|
|Pen contact with eraser button pressed|5|32|

## <span>Try Pointer Events Today</span>

You can tell if a browser supports Pointer Events by checking the `navigator.PointerEnabled` attribute:

``` html
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title></title>
    <script type="text/javascript">
```

``` js
        function init() {
            if ( (navigator.pointerEnabled) || (navigator.msPointerEnabled) ) {
                document.getElementById("dvPointerStatus").innerHTML =
                    "This browser supports Pointer Events :)<br />and supports " +
                    navigator.maxTouchPoints + " simultaneous touch contacts.";
            } else {
                document.getElementById("dvPointerStatus").innerHTML =
                    "This browser does not support Pointer Events. :("
            }
        }
```

``` html
    </script>
</head>
<body onload="init()">
    <p>Checking your browser...</p>
    <div id="dvPointerStatus"></div>
</body>
</html>
```

 Also shown in the above example is how to use the `navigator.maxTouchPoints` attribute to check the maximum number of touch points the hardware supports.

### <span>Webkit With Pointer Events Patch</span>

As of February 2013, builds of WebKit with the Pointer Events patch for OSX and Windows are linked from this blog post by appendTo: <http://appendto.com/blog/2013/02/prototype-chromium-build-with-support-for-ms-pointer-events/>

### <span>Internet Explorer 10</span>

A version of Pointer Events was implemented in IE10 and Pointer Events are prefixed with *MS* (for Microsoft.)

IE10 is included with Windows 8 and Windows Server 2012.

IE10 for Windows 7 or Windows Server 2008 can be downloaded from: <http://windows.microsoft.com/en-US/internet-explorer/downloads/ie-10/worldwide-languages>

## <span>Further Reading</span>

If you're interested in the W3C standardization process for Pointer Events, including reading the specification and providing feedback, here are some useful links:

-   Specification: <http://www.w3.org/TR/pointerevents/>
-   Pointer Events Working Group: <http://www.w3.org/2012/pointerevents/>
-   Working Group Charter: <http://www.w3.org/2012/pointerevents/charter/>
-   Working Group Email List: [mailto:public-pointer-events@w3.org](mailto:public-pointer-events@w3.org)
-   Working Group Email List Archive: <http://lists.w3.org/Archives/Public/public-pointer-events/>

To provide feedback to the working group, send [email to the Pointer Events WG](mailto:public-pointer-events@w3.org).

If you're interested in the patch that adds Pointer Events to WebKit, see:

-   2013-02-11 (AppendTo Blog): [Prototype Chromium build with support for MS Pointer Events](http://appendto.com/blog/2013/02/prototype-chromium-build-with-support-for-ms-pointer-events/)
-   2012-12-18 (Interoperability @ Microsoft): [Open source release from MS Open Tech: Pointer Events initial prototype for WebKit](http://blogs.msdn.com/b/interoperability/archive/2012/12/18/open-source-release-from-ms-open-tech-pointer-events-initial-prototype-for-webkit.aspx)
-   2012-12-18 (HTML5 Labs): [Pointer Events for WebKit](http://html5labs.interoperabilitybridges.com/prototypes/pointer-events-for-webkit/pointer-events-for-webkit/info)

If you're interested in some of the history and evolution of Pointer Events, visit these links from the IEBlog:

-   2012-11-12 (IEBlog): [W3C Charters Pointer Events Working Group](http://blogs.msdn.com/b/ie/archive/2012/11/12/w3c-charters-pointer-events-working-group.aspx)
-   2012-09-24 (IEBlog): [Towards Interoperable Pointer Events: Evolving Input Events for Multiple Devices](http://blogs.msdn.com/b/ie/archive/2012/09/24/towards-interoperable-pointer-events-evolving-input-events-for-multiple-devices.aspx)
-   2012-04-20 (IEBlog): [Guildelines for Building Touch-friendly Sites](http://blogs.msdn.com/b/ie/archive/2012/04/20/guidelines-for-building-touch-friendly-sites.aspx)
-   2011-09-20 (IEBlog): [Touch Input for IE10 and Metro style Apps](http://blogs.msdn.com/b/ie/archive/2011/09/20/touch-input-for-ie10-and-metro-style-apps.aspx)

Here are a few news articles about Pointer Events:

-   2012-12-20 (NeoWin): <http://www.neowin.net/news/microsoft-offers-pointer-events-specs-to-webkit-developers>
-   2012-12-19 (Ars Technica): <http://arstechnica.com/information-technology/2012/12/microsoft-offers-patches-to-webkit-to-aid-touch-compatibility/>
-   2012-09-24 (The Next Web): <http://thenextweb.com/microsoft/2012/09/24/the-w3c-accepted-published-microsofts-pointer-events-submission/>

## <span>Appendix: Designing for Touch</span>

![Image showing 40px hit targets and 10px spacing](/assets/public/a/a9/TouchGuidelines.png)

There are a few key principles that web designers should keep in-mind when updating pages for modern web browsers:

1.  **There may be no hover** — For touch-only devices like many smartphones, there is no ability to hover without invoking
2.  **Don't make hit targets too small** — Studies by Microsoft indicate about 11mm is a good size hit target
3.  **Have spacing between targets** — Studies also by Microsoft suggest 2mm is a good size for spacing between hit targets

For more information, see: <http://blogs.msdn.com/b/ie/archive/2012/04/20/guidelines-for-building-touch-friendly-sites.aspx>

## <span>Related specifications</span>

[Pointer Events](http://www.w3.org/TR/pointerevents/)
:   Working Draft

## <span>See also</span>

### <span>Related articles</span>

#### <span>Pointer Events</span>

-   **Pointer Events Primer**

-   [releasePointerCapture](/dom/Element/releasePointerCapture)

-   [setPointerCapture](/dom/Element/setPointerCapture)

-   [maxTouchPoints](/dom/Navigator/maxTouchPoints)

-   [pointerEnabled](/dom/Navigator/pointerEnabled)

-   [Introduction to multi-touch Web development](/tutorials/mobile_touch)
