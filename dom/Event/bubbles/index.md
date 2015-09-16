---
title: bubbles
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs examples and compat'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Event
    href: /dom/Event
  return:
    predicate: 'Returns an object of type '
    value: Boolean
    href: /dom/Event
standardization_status: 'W3C Working Draft'
summary: 'Gets a value that indicates whether an event propagates up from the event target.'
tags:
  - API
  - Object
  - Properties
  - DOM
  - DOMEvents
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/MouseWheelEvent
uri: dom/Event/bubbles

---
## Summary

Gets a value that indicates whether an event propagates up from the event target.

Property of [dom/Event](/dom/Event)[dom/Event](/dom/Event)

## Syntax

**Note**: This property is read-only.

``` js
var bubbles = event.bubbles;
```

## Return Value

Returns an object of type BooleanBoolean

Whether the event propagates upward from the event target.

**Needs Examples**: This section should include examples.

## Notes

When you create a custom event by using the [**createEvent**](/dom/Document/createEvent) method, you can set the **bubbles** property by using the [**initEvent**](/dom/Event/initEvent) method.

## Related specifications

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
