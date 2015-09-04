---
title: bubbles
tags:
  - API
  - Object
  - Properties
  - DOM
  - DOMEvents
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs examples and compat'
summary: 'Gets a value that indicates whether an event propagates up from the event target.'
uri: dom/Event/bubbles
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/MouseWheelEvent

---
# bubbles

## Summary

Gets a value that indicates whether an event propagates up from the event target.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Event](/dom/Event)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var bubbles = event.bubbles;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

Whether the event propagates upward from the event target.

**Needs Examples**: This section should include examples.

## Notes

When you create a custom event by using the [**createEvent**](/dom/Document/createEvent) method, you can set the **bubbles** property by using the [**initEvent**](/dom/Event/initEvent) method.

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
-   `cancelable`
-   `stopPropagation`
-   `stopImmediatePropagation`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

