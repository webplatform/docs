---
title: isTrusted
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example, spec reference, standardization status'
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
summary: 'Gets a value that indicates whether a trusted event source created an event.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Event/isTrusted

---
## <span>Summary</span>

Gets a value that indicates whether a trusted event source created an event.

Property of [dom/Event](/dom/Event)[dom/Event](/dom/Event)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var isTrusted = event.isTrusted;
```

## <span>Return Value</span>

Returns an object of type BooleanBoolean

Whether the event was created by a trusted source.

**Needs Examples**: This section should include examples.

## <span>Usage</span>

     Use this property to determine whether a script created the event, rather than a trusted source (such as a user agent).

## <span>See also</span>

### <span>Related pages (MSDN)</span>

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
