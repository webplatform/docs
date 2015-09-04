---
title: type
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs example'
summary: 'Gets the name of an event.'
uri: dom/Event/type

---
# type

## Summary

Gets the name of an event.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Event](/dom/Event)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var eventType = event.type;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The name of the event.

**Needs Examples**: This section should include examples.

## Notes

The **type** property of the event depends on the event. This property can be a standard event type, or it can be a custom user-defined event that you created by using the [**createEvent**](/dom/Document/createEvent) and [**initEvent**](/dom/Event/initEvent) methods.

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

