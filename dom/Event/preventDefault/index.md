---
title: 'preventDefault'
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
summary: 'Cancels the default action of an event, if possible.'
tags:
  - API_Object_Methods
  - DOM
  - Needs_Examples
uri: dom/Event/preventDefault

---
## Summary

Cancels the default action of an event, if possible.

Method of [dom/Event](/dom/Event)[dom/Event](/dom/Event)

## Syntax

``` js
 event.preventDefault();
```

## Return Value

No return value

## Usage

     Use this method to prevent the default action of a cancelable event. For example, prevent the browser from navigating when clicking on a a element.

An event is cancelable if its [cancelable](/dom/Event/cancelable) property returns true.

## Notes

If the event cannot be canceled, this method has no effect.

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
