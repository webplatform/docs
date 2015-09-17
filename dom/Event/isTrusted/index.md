---
title: 'isTrusted'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Event
    href: /dom/Event
  return:
    predicate: 'Returns an object of type '
    value: Boolean
    href: /dom/Event
summary: 'Gets a value that indicates whether a trusted event source created an event.'
tags:
  - API_Object_Properties
  - DOM
  - Needs_Examples
uri: dom/Event/isTrusted

---
## Summary

Gets a value that indicates whether a trusted event source created an event.

Property of [dom/Event](/dom/Event)[dom/Event](/dom/Event)

## Syntax

**Note**: This property is read-only.

``` js
var isTrusted = event.isTrusted;
```

## Return Value

Returns an object of type BooleanBoolean

Whether the event was created by a trusted source.

## Usage

     Use this property to determine whether a script created the event, rather than a trusted source (such as a user agent).

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
