---
title: cancelable
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
summary: 'Gets a value that indicates whether you can cancel an event''s default action.'
tags:
  - API
  - Object
  - Properties
  - DOM
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/MouseWheelEvent
uri: dom/Event/cancelable

---
## Summary

Gets a value that indicates whether you can cancel an event's default action.

Property of [dom/Event](/dom/Event)[dom/Event](/dom/Event)

## Syntax

**Note**: This property is read-only.

``` js
var cancelable = event.cancelable;
```

## Return Value

Returns an object of type BooleanBoolean

Whether the event's default action can be canceled.

**Needs Examples**: This section should include examples.

## Notes

If you cannot cancel the event, calling [**preventDefault**](/dom/Event/preventDefault) has no effect. When you create a custom event by using the [**createEvent**](/dom/Document/createEvent) method, you can set the **cancelable** property by using the [**initEvent**](/dom/Event/initEvent) method.

## Related specifications

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## See also

### Related pages

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
