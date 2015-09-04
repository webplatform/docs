---
title: isTrusted
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'Gets a value that indicates whether a trusted event source created an event.'
uri: dom/Event/isTrusted

---
# isTrusted

## Summary

Gets a value that indicates whether a trusted event source created an event.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Event](/dom/Event)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var isTrusted = event.isTrusted;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

Whether the event was created by a trusted source.

**Needs Examples**: This section should include examples.

## Usage

     Use this property to determine whether a script created the event, rather than a trusted source (such as a user agent).

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
-   `WheelEvent`
-   `MutationEvent`
-   `StorageEvent`
-   `TextEvent`
-   `UIEvent`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

