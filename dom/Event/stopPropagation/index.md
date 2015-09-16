---
title: stopPropagation
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
summary: 'Prevents propagation of an event beyond the current target.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Event/stopPropagation

---
## Summary

Prevents propagation of an event beyond the current target.

Method of [dom/Event](/dom/Event)[dom/Event](/dom/Event)

## Syntax

``` js
 event.stopPropagation();
```

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Usage

     Use this method to stop event propagation in the capturing or bubbling event phase.

## Notes

The event dispatches to all event listeners on the current target (regardless of capturing or bubbling) before the event flow stops. To completely prevent any remaining handlers from running, use the [**stopImmediatePropagation**](/dom/Event/stopImmediatePropagation) method instead.

## Related specifications

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## See also

### Related pages (MSDN)

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
-   `MutationEvent`
-   `StorageEvent`
-   `TextEvent`
-   `UIEvent`
