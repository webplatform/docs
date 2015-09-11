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
## <span>Summary</span>

Gets a value that indicates whether an event propagates up from the event target.

Property of [dom/Event](/dom/Event)[dom/Event](/dom/Event)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var bubbles = event.bubbles;
```

## <span>Return Value</span>

Returns an object of type BooleanBoolean

Whether the event propagates upward from the event target.

**Needs Examples**: This section should include examples.

## <span>Notes</span>

When you create a custom event by using the [**createEvent**](/dom/Document/createEvent) method, you can set the **bubbles** property by using the [**initEvent**](/dom/Event/initEvent) method.

## <span>Related specifications</span>

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## <span>See also</span>

### <span>Related pages (MSDN)</span>

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
