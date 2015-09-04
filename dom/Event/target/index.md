---
title: target
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs example'
summary: 'Gets the element that is the original target of the event.'
uri: dom/Event/target

---
# target

## Summary

Gets the element that is the original target of the event.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Event](/dom/Event)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var originalTargetElement = event.target;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">DOM Node</span></span>

The original target element of the event.

**Needs Examples**: This section should include examples.

## Usage

     Use this property to determine the original element on which the event was dispatched.

## Notes

The [**currentTarget**](/dom/Event/currentTarget) property returns the element that the event handlers are being processed for during the capturing and bubbling phases.

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

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

