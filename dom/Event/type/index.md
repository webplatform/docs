---
title: type
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Event
    href: /dom/Event
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Event
standardization_status: 'W3C Working Draft'
summary: 'Gets the name of an event.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Event/type

---
## Summary

Gets the name of an event.

Property of [dom/Event](/dom/Event)[dom/Event](/dom/Event)

## Syntax

**Note**: This property is read-only.

``` js
var eventType = event.type;
```

## Return Value

Returns an object of type StringString

The name of the event.

**Needs Examples**: This section should include examples.

## Notes

The **type** property of the event depends on the event. This property can be a standard event type, or it can be a custom user-defined event that you created by using the [**createEvent**](/dom/Document/createEvent) and [**initEvent**](/dom/Event/initEvent) methods.

## Related specifications

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
