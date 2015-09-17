---
title: 'currentTarget'
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
    value: 'DOM Node'
    href: /dom/Event
standardization_status: 'W3C Working Draft'
summary: 'Gets the event target that is currently being processed.'
tags:
  - API_Object_Properties
  - DOM
  - Needs_Examples
uri: dom/Event/currentTarget

---
## Summary

Gets the event target that is currently being processed.

Property of [dom/Event](/dom/Event)[dom/Event](/dom/Event)

## Syntax

**Note**: This property is read-only.

``` js
var currentTargetElement = event.currentTarget;
```

## Return Value

Returns an object of type DOM NodeDOM Node

The current target of the event.

## Usage

     Use this property to get the element for which the current event handler is being processed, during the capturing and bubbling phases.

## Notes

The [**target**](/dom/Event/target) property returns the element that originally received an event. At event phase `AT_TARGET`, the **currentTarget** and **target** objects are the same object.

## Related specifications

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## See also

### Related pages

-   SVGZoomEvent[SVGZoomEvent](/svg/objects/SVGZoom)
-   BeforeUnloadEvent[BeforeUnloadEvent](/dom/BeforeUnloadEvent)
-   CompositionEvent[CompositionEvent](/dom/CompositionEvent)
-   CustomEvent[CustomEvent](/dom/CustomEvent)
-   Event[Event](/dom/Event)
-   DragEvent[DragEvent](/dom/DragEvent)
-   FocusEvent[FocusEvent](/dom/FocusEvent)
-   KeyboardEvent[KeyboardEvent](/dom/KeyboardEvent)
-   MessageEvent[MessageEvent](/dom/MessageEvent)
-   MouseEvent[MouseEvent](/dom/MouseEvent)
-   WheelEvent[WheelEvent](/dom/WheelEvent)
-   MutationEvent[MutationEvent](/dom/MutationEvent)
-   StorageEvent[StorageEvent](/dom/StorageEvent)
-   TextEvent[TextEvent](/dom/TextEvent)
-   UIEvent[UIEvent](/dom/UIEvent)
-   eventPhase[eventPhase](/dom/Event/eventPhase)
