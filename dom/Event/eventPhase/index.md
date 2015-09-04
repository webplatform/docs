---
title: eventPhase
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs example'
summary: 'Gets the event phase that is being evaluated.'
uri: dom/Event/eventPhase

---
# eventPhase

## Summary

Gets the event phase that is being evaluated.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Event](/dom/Event)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var eventPhase = event.eventPhase;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

0 is the initial and final phase (NONE), which means an event has not been dispatched, or the event is done dispatching. 1 is the capturing phase (CAPTURING\_PHASE), which means it is currently running the capturing event handlers. 2 is the at target phase (AT\_TARGET), which means it is currently running the event handlers that were added to the same element the event on which was dispatched. 3 is the bubbling phase (BUBBLING\_PHASE), which means it is currently running event handlers of parent nodes of the original target element.

**Needs Examples**: This section should include examples.

## Notes

During the capturing phase, events are dispatched to parent elements before objects that are lower in the hierarchy. Next, during the bubbling phase, events are dispatched to target elements followed by parent objects. The event phase is `AT_TARGET` when the element that receives the event ([**target**](/dom/Event/target)) is the same element as the element that is processing the event ([**currentTarget**](/dom/Event/currentTarget)). The target element receives both capture and bubble events if both are registered.

## Related specifications

Specification
:   Status
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

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

