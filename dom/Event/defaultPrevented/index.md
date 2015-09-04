---
title: defaultPrevented
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs example'
summary: 'Gets whether the default action should be canceled.'
uri: dom/Event/defaultPrevented

---
# defaultPrevented

## Summary

Gets whether the default action should be canceled.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Event](/dom/Event)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var shouldPreventDefault = event.defaultPrevented;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

Whether the default action should be canceled.

**Needs Examples**: This section should include examples.

## Usage

     Use this property to determine whether the default action of an event was prevented.

## Notes

You can set the value of this property to **true** while processing an event, by calling the [**preventDefault**](/dom/Event/preventDefault) method. If the event was initialized with the *cancelable* parameter of [**initEvent**](/dom/Event/initEvent) set to false, the default action cannot be prevented.

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
-   `Event`
-   `DragEvent`
-   `FocusEvent`
-   `KeyboardEvent`
-   `MessageEvent`
-   `MouseEvent`
-   `WheelEvent`
-   `MutationEvent`
-   `StorageEvent`
-   `TextEvent`
-   `UIEvent`
-   `Reference`
-   `cancelable`
-   `preventDefault`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

