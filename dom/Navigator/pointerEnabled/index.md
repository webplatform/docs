---
title: 'pointerEnabled'
attributions:
  - 'Microsoft Developer Network: [[navigator.pointerEnabled](http://msdn.microsoft.com/en-us/library/ie/hh972895(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Navigator
    href: /dom/Navigator
  return:
    predicate: 'Returns an object of type '
    value: Boolean
    href: /dom/Navigator
standardization_status: Deprecated
summary: "Indicates if the browser will fire pointer events for pointing input.\n"
tags:
  - API_Object_Properties
uri: dom/Navigator/pointerEnabled

---
## Summary

Indicates if the browser will fire pointer events for pointing input.

In late 2013, pointerEnabled was removed from the specification as checking PointerEvent in Window object is sufficient for feature detection. Do not use this property and use PointerEvent instead.

Property of [dom/Navigator](/dom/Navigator)[dom/Navigator](/dom/Navigator)

## Syntax

**Note**: This property is read-only.

``` js
var result = navigator.pointerEnabled;
```

## Return Value

Returns an object of type BooleanBoolean

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

## Notes

In late 2013, pointerEnabled was removed from the specification as checking PointerEvent in Window object is sufficient for feature detection. Do not use this property and use PointerEvent instead.

## Related specifications

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

-   [Introduction to multi-touch Web development](/tutorials/mobile_touch)

