---
title: 'maxTouchPoints'
attributions:
  - 'Microsoft Developer Network: [[maxTouchPoints property](http://msdn.microsoft.com/en-us/library/ie/hh772144(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Navigator
    href: /dom/Navigator
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /dom/Navigator
standardization_status: 'W3C Working Draft'
summary: 'The maximum number of simultaneous touch contacts supported by the device.'
tags:
  - API
  - Object
  - Properties
uri: dom/Navigator/maxTouchPoints

---
## Summary

The maximum number of simultaneous touch contacts supported by the device.

Property of [dom/Navigator](/dom/Navigator)[dom/Navigator](/dom/Navigator)

## Syntax

**Note**: This property is read-only.

``` js
var result = navigator.maxTouchPoints;
```

## Return Value

Returns an object of type NumberNumber

## Examples

Basic HTML5 Canvas painting application

``` js
<style>
  /* Disable intrinsic user agent touch behaviors (such as panning or zooming) so
  that all events are given to the application instead. */

  html {
    touch-action: none;
  }
</style>

<canvas id="drawSurface" width="500px" height="500px" style="border:1px solid black;"></canvas>

<script type='text/javascript'>
window.addEventListener('load', function() {
  var canvas = document.getElementById("drawSurface"),
  context = canvas.getContext("2d");
  if (window.navigator.pointerEnabled) {
    canvas.addEventListener("pointermove", paint, false);
    if(window.navigator.maxTouchPoints>1)
        alert("Your user agent and hardware support multi-touch!");
  }
  else {
    //Provide fallback for user agents that do not support Pointer Events
    canvas.addEventListener("mousemove", paint, false);
  }
  function paint(event) {
    if(event.buttons>0)
        context.fillRect(event.clientX, event.clientY, 5, 5);
  }
});
```

## Usage

     In the case of devices with multiple digitizers (e.g. multiple touchscreens), the value must be the maximum of the set of maximum supported contacts by each individual digitizer.

For example, suppose a device has 3 touchscreens, which support 2, 5, and 10 simultaneous touch contacts, respectively. The value of *maxTouchPoints* is 10.

## Related specifications

[Pointer Events](http://www.w3.org/TR/pointerevents)
:   Working Draft

## See also

### Related articles

#### Pointer Events

-   [Pointer Events Primer](/concepts/Pointer_Events)

-   [releasePointerCapture](/dom/Element/releasePointerCapture)

-   [setPointerCapture](/dom/Element/setPointerCapture)

-   **maxTouchPoints**

-   [pointerEnabled](/dom/Navigator/pointerEnabled)

-   [Introduction to multi-touch Web development](/tutorials/mobile_touch)

