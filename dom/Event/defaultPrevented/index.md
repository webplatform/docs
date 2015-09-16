---
title: defaultPrevented
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
    value: Boolean
    href: /dom/Event
standardization_status: 'W3C Working Draft'
summary: 'Gets whether the default action should be canceled.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Event/defaultPrevented

---
## Summary

Gets whether the default action should be canceled.

Property of [dom/Event](/dom/Event)[dom/Event](/dom/Event)

## Syntax

**Note**: This property is read-only.

``` js
var shouldPreventDefault = event.defaultPrevented;
```

## Return Value

Returns an object of type BooleanBoolean

Whether the default action should be canceled.

**Needs Examples**: This section should include examples.

## Usage

     Use this property to determine whether the default action of an event was prevented.

## Notes

You can set the value of this property to **true** while processing an event, by calling the [**preventDefault**](/dom/Event/preventDefault) method. If the event was initialized with the *cancelable* parameter of [**initEvent**](/dom/Event/initEvent) set to false, the default action cannot be prevented.

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
-   `WheelEvent`
-   `MutationEvent`
-   `StorageEvent`
-   `TextEvent`
-   `UIEvent`
-   `Reference`
-   `cancelable`
-   `preventDefault`
