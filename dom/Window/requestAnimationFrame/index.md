---
title: requestAnimationFrame
tags:
  - API
  - Object
  - Methods
  - DOM
standardization_status: Mixed
notes:
  - 'Not part of user_timing, resource_timing, or navigation_timing interfaces.'
summary: 'A method to invoke at the optimal time a callback to update the frame of an animation.'
uri: dom/Window/requestAnimationFrame

---
# requestAnimationFrame

## Summary

A method to invoke at the optimal time a callback to update the frame of an animation.

*Method of [dom/Window](/dom/Window)*

## Syntax

``` {.js}
var handle = window.requestAnimationFrame(/* see parameter list */);
```

## Parameters

### callback

 Data-typeÂ
:   function

 The animation code to be run when the system is ready.

## Return Value

Returns an object of type Number.

A handle or ID to the animationFrame request that can be used to cancel the request if needed.

## Examples

``` {.html}
<!DOCTYPE html>
<html>
<head>
<title>requestAnimationFrame</title>
<style type="text/css">
div { position: absolute; left: 10px; top:100px; padding: 50px;
  background: crimson; color: white }
</style>

</head>
<body>

<div id="animated">Hello there.</div>
<button onclick="start()">Start</button>
<button onclick="stop()">Stop</button>
    <script type="text/javascript">
        var elm = document.getElementById("animated");
        var stopped;
        var requestId = 0;
        var starttime;

        function render(time) {
            // set left style to a function of time.
          if (!stopped) {
            elm.style.left = ((Date.now() - starttime) / 4Â % 600) + "px";
            requestId = window.requestAnimationFrame(render);
            }
        }

        function start() {
            starttime = Date.now();
            requestId = window.requestAnimationFrame(render);
            stopped = false;
        }
        function stop() {
            if (requestId) {
                window.cancelAnimationFrame(requestId);
            }
            stopped = true;
        }


</script>


</body></html>
```

## Notes

Unlike older animation techniques based on [**setTimeout**](/dom/Window/setTimeout) and [**setInterval**](/dom/Window/setInterval) methods, **requestAnimationFrame** based animation occurs when the system is ready. This leads to smoother animations and less power consumption than animations because **requestAnimationFrame** takes the visibility of the web application and the refresh rate of the display into account, The **requestAnimationFrame** method creates only a single animation request. To create continous animation, a new request must be registered for each frame. To cancel an animation request before the animation function is called back, use [**cancelAnimationFrame**](/dom/Window/cancelAnimationFrame).

## Related specifications

Specification
:   Status
[Timing control for script-based animations](http://www.w3.org/TR/animation-timing/)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[requestAnimationFrame](http://msdn.microsoft.com/en-us/library/ie/hh773174(v=vs.85).aspx) Article]

