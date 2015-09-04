---
title: preventDefault
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs example'
summary: 'Cancels the default action of an event, if possible.'
uri: dom/Event/preventDefault

---
# preventDefault

## Summary

Cancels the default action of an event, if possible.

*Method of [dom/Event](/dom/Event)*

## Syntax

``` {.js}
 event.preventDefault();
```

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Usage

     Use this method to prevent the default action of a cancelable event. For example, prevent the browser from navigating when clicking on a a element.

An event is cancelable if its [cancelable](/dom/Event/cancelable) property returns true.

## Notes

If the event cannot be canceled, this method has no effect.

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
-   `WheelEvent`
-   `MutationEvent`
-   `StorageEvent`
-   `TextEvent`
-   `UIEvent`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

