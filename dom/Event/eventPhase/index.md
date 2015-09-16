---
title: eventPhase
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Event
    href: /dom/Event
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /dom/Event
standardization_status: 'W3C Working Draft'
summary: 'Gets the event phase that is being evaluated.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Event/eventPhase

---
## Summary

Gets the event phase that is being evaluated.

Property of [dom/Event](/dom/Event)[dom/Event](/dom/Event)

## Syntax

**Note**: This property is read-only.

``` js
var eventPhase = event.eventPhase;
```

## Return Value

Returns an object of type NumberNumber

0 is the initial and final phase (NONE), which means an event has not been dispatched, or the event is done dispatching. 1 is the capturing phase (CAPTURING\_PHASE), which means it is currently running the capturing event handlers. 2 is the at target phase (AT\_TARGET), which means it is currently running the event handlers that were added to the same element the event on which was dispatched. 3 is the bubbling phase (BUBBLING\_PHASE), which means it is currently running event handlers of parent nodes of the original target element.

**Needs Examples**: This section should include examples.

## Notes

During the capturing phase, events are dispatched to parent elements before objects that are lower in the hierarchy. Next, during the bubbling phase, events are dispatched to target elements followed by parent objects. The event phase is `AT_TARGET` when the element that receives the event ([**target**](/dom/Event/target)) is the same element as the element that is processing the event ([**currentTarget**](/dom/Event/currentTarget)). The target element receives both capture and bubble events if both are registered.

## Related specifications

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## See also

### Related pages (MSDN)

-   `SVGZoomEvent`
-   `BeforeUnloadEvent`
-   `CompositionEvent`
-   `CustomEvent`
-   `Event`
-   `DragEvent`
-   `FocusEvent`
-   `KeyboardEvent`
-   `MessageEvent`
-   `MouseEvent`
-   `WheelEvent`
-   `MutationEvent`
-   `StorageEvent`
-   `TextEvent`
-   `UIEvent`
