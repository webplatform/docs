---
title: cancelAnimationFrame
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[cancelAnimationFrame](https://developer.mozilla.org/en-US/docs/Web/API/Window.cancelAnimationFrame) Article]'
  - 'Microsoft Developer Network: [[cancelAnimationFrame Method](http://msdn.microsoft.com/en-us/library/windows/apps/hh453388.aspx) Article]'
notes:
  - 'Not part of user_timing, resource_timing, or navigation_timing interfaces.'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Window
    href: /dom/Window
standardization_status: Non-Standard
summary: 'Cancels a requestAnimationFrame request'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Window/cancelAnimationFrame

---
## Summary

Cancels a requestAnimationFrame request

Method of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## Syntax

``` js
 window.cancelAnimationFrame(/* see parameter list */);
```

## Parameters

### handle

 Data-type
:   any

 A handle of the animation request to cancel. The handle is the value returned by [**requestAnimationFrame**](/dom/Window/requestAnimationFrame).

## Return Value

No return value

## Examples

``` html
<!DOCTYPE html>
<html>
<head>
<title>Script-based animation using requestAnimationFrame</title>
<style type="text/css">
div { position: absolute; left: 10px; top:100px; padding: 50px;
  background: crimson; color: white }
</style>

</head>
<body>

<div id="animated" style="left: 549.5px;">Hello there.</div>
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
            elm.style.left = ((Date.now() - starttime) / 4 % 600) + "px";
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
</body>
</html>
```

## Usage

     Script based animations.

### Syntax

### Standards information

-   [Timing control for script-based animations](http://go.microsoft.com/fwlink/p/?linkid=229562)
