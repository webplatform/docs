---
title: pointermove
tags:
  - Events
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Dispatched when a pointer changes coordinates, button state, pressure, tilt, or contact geometry (e.g. width and height).'
uri: dom/PointerEvent/pointermove

---
# pointermove

## Summary

Dispatched when a pointer changes coordinates, button state, pressure, tilt, or contact geometry (e.g. width and height).

## Overview Table

Synchronous
:   Yes
Bubbles
:   Yes
Target
:   dom/Element
Cancelable
:   Yes
Default action
:   Varies: when the pointer is primary, all default actions of the [mousemove](/dom/MouseEvent/mousemove) event

## Examples

``` {.js}
element.addEventListener("pointermove", handler, useCapture) ;
```

## Related specifications

Specification
:   Status
[Pointer Events](http://www.w3.org/TR/pointerevents)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[pointermove Event](http://msdn.microsoft.com/en-us/library/ie/hh771911(v=vs.85).aspx) Article]

