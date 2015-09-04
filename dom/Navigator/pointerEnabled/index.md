---
title: pointerEnabled
tags:
  - API
  - Object
  - Properties
readiness: 'Ready to Use'
standardization_status: Deprecated
summary: "Indicates if the browser will fire pointer events for pointing input.\n"
uri: dom/Navigator/pointerEnabled

---
# pointerEnabled

## Summary

Indicates if the browser will fire pointer events for pointing input.

In late 2013, pointerEnabled was removed from the specification as checking PointerEvent in Window object is sufficient for feature detection. Do not use this property and use PointerEvent instead.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Navigator](/dom/Navigator)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = navigator.pointerEnabled;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

## Examples

Basic HTML5 Canvas painting application

``` {.js}
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

## Notes

In late 2013, pointerEnabled was removed from the specification as checking PointerEvent in Window object is sufficient for feature detection. Do not use this property and use PointerEvent instead.

## Related specifications

Specification
:   Status
[Pointer Events](http://www.w3.org/TR/pointerevents/)
:   Candidate Recommendation

## See also

### Related articles

#### Pointer Events

-   [Pointer Events Primer](/concepts/Pointer_Events)

-   [releasePointerCapture](/dom/Element/releasePointerCapture)

-   [setPointerCapture](/dom/Element/setPointerCapture)

-   [maxTouchPoints](/dom/Navigator/maxTouchPoints)

-   **pointerEnabled**

-   [PointerEvent](/dom/PointerEvent)

-   [Introduction to multi-touch Web development](/tutorials/mobile_touch)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[navigator.pointerEnabled](http://msdn.microsoft.com/en-us/library/ie/hh972895(v=vs.85).aspx) Article]

