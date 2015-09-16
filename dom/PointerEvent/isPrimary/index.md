---
title: isPrimary
attributions:
  - 'Microsoft Developer Network: [[isPrimary Property](http://msdn.microsoft.com/en-us/library/ie/jj152130(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/PointerEvent
    href: /dom/PointerEvent
standardization_status: 'W3C Working Draft'
summary: 'Returns whether the pointer associated with the event is the primary pointer for the current mouse, touch, or pen interaction.'
tags:
  - API
  - Object
  - Properties
uri: dom/PointerEvent/isPrimary

---
## Summary

Returns whether the pointer associated with the event is the primary pointer for the current mouse, touch, or pen interaction.

Property of [dom/PointerEvent](/dom/PointerEvent)[dom/PointerEvent](/dom/PointerEvent)

## Syntax

**Note**: This property is read-only.

``` js
var result = event.isPrimary;
```

**Needs Examples**: This section should include examples.

## Usage

     In a multi-pointer (e.g. multi-touch) scenario, the primary pointer is used to identify a master pointer amongst the set of active pointers. This pointer is the one that will produce compatibility mouse events. It is also useful when single-pointer interaction is desired by an author.

When dispatching a pointer event, a pointer is considered primary if:

-   The pointer represents a mouse device.
-   The pointer represents *primary touch input*, where its pointerdown event was dispatched when no other active pointers representing touch input existed.
-   The pointer represents *primary pen input*, where its pointerdown event was dispatched when no other active pointers representing pen input existed.

## Notes

In some platforms, the primary pointer is determined using all active pointers on the device including those not targeted at the user agent (e.g. in another application). This means it is possible for the user agent to fire pointer events in which no pointer is marked as the primary pointer. For example, if the first touch interaction is targeted outside the user agent and a secondary (multi-touch) touch interaction is targeted inside the user agent, then the user agent fires pointer events for the second contact with a value of false for isPrimary.

## Related specifications

[Pointer Events](http://www.w3.org/TR/pointerevents)
:   Working Draft

