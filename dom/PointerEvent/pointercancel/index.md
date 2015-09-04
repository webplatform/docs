---
title: pointercancel
tags:
  - Events
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Dispatched when either (1) the user agent has determined that a pointer is unlikely to continue to produce events (e.g., due to a hardware event), or (2) after having fired the pointerdown event, the pointer is subsequently used to manipulate the page viewport (e.g., panning or zooming).'
uri: dom/PointerEvent/pointercancel

---
# pointercancel

## Summary

Dispatched when either (1) the user agent has determined that a pointer is unlikely to continue to produce events (e.g., due to a hardware event), or (2) after having fired the pointerdown event, the pointer is subsequently used to manipulate the page viewport (e.g., panning or zooming).

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
:   None

A user agent will also fire a [pointerout](/dom/PointerEvent/pointerout) event after firing the pointercancel event.

## Examples

``` {.js}
element.addEventListener("pointercancel", handler, useCapture) ;
```

## Usage

     This event occurs when the pointer (touch or pen contact) is removed from the system. Here are common reasons why this might happen:

-   A touch contact is canceled by a pen coming into range of the surface.
-   The device doesn't report an active contact for more than 100ms.
-   A mapping for a device's monitor changes while contacts are active. For example, the user changes the position of a screen in a two screen configuration.
-   The desktop is locked or the user logged off.
-   The number of simultaneous contacts exceeds the number that the device can support. For example, if a device supports only two contact points, if the user has two fingers on a surface, and then touches it with a third finger, this event is raised.

## Notes

When the pointercancel event is raised for a pointer, the app won’t receive any other events for that pointer, including pointerup . The app should perform any necessary cleanup as required for the pointer. For example, if the app maintains a pointer list, the app should remove the pointer from the list.

You shouldn't treat this event like an pointerup event. When a pointer is removed, the app should cancel any ongoing work. The following example shows how you might handle pointer events if the target is a button:

## Related specifications

Specification
:   Status
[Pointer Events](http://www.w3.org/TR/pointerevents)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[pointercancel Event](http://msdn.microsoft.com/en-us/library/ie/hh846776(v=vs.85).aspx) Article]

