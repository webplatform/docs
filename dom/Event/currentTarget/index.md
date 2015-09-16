---
title: currentTarget
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
    value: 'DOM Node'
    href: /dom/Event
standardization_status: 'W3C Working Draft'
summary: 'Gets the event target that is currently being processed.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Event/currentTarget

---
## Summary

Gets the event target that is currently being processed.

Property of [dom/Event](/dom/Event)[dom/Event](/dom/Event)

## Syntax

**Note**: This property is read-only.

``` js
var currentTargetElement = event.currentTarget;
```

## Return Value

Returns an object of type DOM NodeDOM Node

The current target of the event.

**Needs Examples**: This section should include examples.

## Usage

     Use this property to get the element for which the current event handler is being processed, during the capturing and bubbling phases.

## Notes

The [**target**](/dom/Event/target) property returns the element that originally received an event. At event phase `AT_TARGET`, the **currentTarget** and **target** objects are the same object.

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
-   `WheelEvent`
-   `MutationEvent`
-   `StorageEvent`
-   `TextEvent`
-   `UIEvent`
-   `eventPhase`
