---
title: 'stopImmediatePropagation'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Event
    href: /dom/Event
standardization_status: 'W3C Working Draft'
summary: 'Prevents any further propagation of an event.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Event/stopImmediatePropagation

---
## Summary

Prevents any further propagation of an event.

Method of [dom/Event](/dom/Event)[dom/Event](/dom/Event)

## Syntax

``` js
 event.stopImmediatePropagation();
```

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Usage

     Use this method to prevent any further dispatch of the event, even if additional event handlers remain on the target element.

## Notes

To allow the remaining handlers to run, use the [**stopPropagation**](/dom/Event/stopPropagation) method instead.

## Related specifications

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## See also

### Related pages

-   SVGZoomEvent[SVGZoomEvent](/svg/objects/SVGZoom)
-   BeforeUnloadEvent[BeforeUnloadEvent](/dom/BeforeUnloadEvent)
-   CompositionEvent[CompositionEvent](/dom/CompositionEvent)
-   CustomEvent[CustomEvent](/dom/CustomEvent)
-   DragEvent[DragEvent](/dom/DragEvent)
-   Event[Event](/dom/Event)
-   FocusEvent[FocusEvent](/dom/FocusEvent)
-   KeyboardEvent[KeyboardEvent](/dom/KeyboardEvent)
-   MessageEvent[MessageEvent](/dom/MessageEvent)
-   MouseEvent[MouseEvent](/dom/MouseEvent)
-   WheelEvent[WheelEvent](/dom/WheelEvent)
-   MutationEvent[MutationEvent](/dom/MutationEvent)
-   StorageEvent[StorageEvent](/dom/StorageEvent)
-   TextEvent[TextEvent](/dom/TextEvent)
-   UIEvent[UIEvent](/dom/UIEvent)
