---
title: pointerover
tags:
  - Events
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Dispatched when a pointing device is moved into the hit test boundaries of an element. Also dispatched prior to a pointerdown event for devices that do not support hover.'
uri: dom/PointerEvent/pointerover

---
# pointerover

## Summary

Dispatched when a pointing device is moved into the hit test boundaries of an element. Also dispatched prior to a pointerdown event for devices that do not support hover.

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
:   Varies: when the pointer is primary, all default actions of the [mouseover](/dom/MouseEvent/mouseover) event

## Examples

``` {.js}
element.addEventListener("pointerover", handler, useCapture);
```

## Related specifications

Specification
:   Status
[Pointer Events](http://www.w3.org/TR/pointerevents)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[pointerover Event](http://msdn.microsoft.com/en-us/library/ie/hh771913(v=vs.85).aspx) Article]

