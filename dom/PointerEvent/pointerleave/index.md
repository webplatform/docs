---
title: pointerleave
tags:
  - Events
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Dispatched when a pointing device is moved off of the hit test boundaries of an element and all of its descendants, including as a result of a pointerup event from a device that does not support hover.'
uri: dom/PointerEvent/pointerleave

---
# pointerleave

## Summary

Dispatched when a pointing device is moved off of the hit test boundaries of an element and all of its descendants, including as a result of a pointerup event from a device that does not support hover.

## Overview Table

Synchronous
:   Yes
Bubbles
:   No
Target
:   dom/Element
Cancelable
:   Yes
Default action
:   Varies: when the pointer is primary, all default actions of the [mouseleave](/dom/MouseEvent/mouseleave) event.

This event type is similar to [pointerout](/dom/PointerEvent/pointerout), but differs in that it does not bubble and that it is not dispatched until the pointing device has left the boundaries of the element and the boundaries of all its children.

## Examples

``` {.js}
element.addEventListener("pointerleave", handler, useCapture) ;
```

## Notes

There are similarities between this event type, the [mouseleave](/dom/MouseEvent/mouseleave) event described in [DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/) and the CSS :hover pseudo-class described in [CSS 2.1](http://www.w3.org/TR/CSS2/). See also the [pointerenter](/dom/PointerEvent/pointerenter) event.

## Related specifications

Specification
:   Status
[Pointer Events](http://www.w3.org/TR/pointerevents)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[pointerleave Event](http://msdn.microsoft.com/en-us/library/ie/dn254945(v=vs.85).aspx) Article]

