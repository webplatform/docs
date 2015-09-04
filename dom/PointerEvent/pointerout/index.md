---
title: pointerout
tags:
  - Events
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: "Dispatched when any of the following occurs:\n"
uri: dom/PointerEvent/pointerout

---
# pointerout

## Summary

Dispatched when any of the following occurs:

-   A pointing device is moved out of the hit test boundaries of an element
-   After firing the [pointerup](/dom/PointerEvent/pointerup) event for a device that does not support hover
-   After firing the [pointercancel](/dom/PointerEvent/pointercancel) event

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
:   Varies: when the pointer is primary, all default actions of the [mouseout](/dom/MouseEvent/mouseout) event

## Examples

``` {.js}
element.addEventListener("pointerout", handler, useCapture) ;
```

## Related specifications

Specification
:   Status
[Pointer Events](http://www.w3.org/TR/pointerevents)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[pointerout Event](http://msdn.microsoft.com/en-us/library/ie/hh771912(v=vs.85).aspx) Article]

