---
title: cancelable
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs examples and compat'
summary: 'Gets a value that indicates whether you can cancel an event''s default action.'
uri: dom/Event/cancelable
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/MouseWheelEvent

---
# cancelable

## Summary

Gets a value that indicates whether you can cancel an event's default action.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Event](/dom/Event)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var cancelable = event.cancelable;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

Whether the event's default action can be canceled.

**Needs Examples**: This section should include examples.

## Notes

If you cannot cancel the event, calling [**preventDefault**](/dom/Event/preventDefault) has no effect. When you create a custom event by using the [**createEvent**](/dom/Document/createEvent) method, you can set the **cancelable** property by using the [**initEvent**](/dom/Event/initEvent) method.

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
-   `MouseWheelEvent`
-   `MutationEvent`
-   `StorageEvent`
-   `TextEvent`
-   `UIEvent`
-   `Reference`
-   `bubbles`
-   `preventDefault`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

