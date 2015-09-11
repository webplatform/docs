---
title: stopImmediatePropagation
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
## <span>Summary</span>

Prevents any further propagation of an event.

Method of [dom/Event](/dom/Event)[dom/Event](/dom/Event)

## <span>Syntax</span>

``` js
 event.stopImmediatePropagation();
```

## <span>Return Value</span>

No return value

**Needs Examples**: This section should include examples.

## <span>Usage</span>

     Use this method to prevent any further dispatch of the event, even if additional event handlers remain on the target element.

## <span>Notes</span>

To allow the remaining handlers to run, use the [**stopPropagation**](/dom/Event/stopPropagation) method instead.

## <span>Related specifications</span>

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `SVGZoomEvent`
-   `BeforeUnloadEvent`
-   `CompositionEvent`
-   `CustomEvent`
-   `DragEvent`
-   `Event`
-   `FocusEvent`
-   `KeyboardEvent`
-   `MessageEvent`
-   `MouseEvent`
-   `WheelEvent`
-   `MutationEvent`
-   `StorageEvent`
-   `TextEvent`
-   `UIEvent`
