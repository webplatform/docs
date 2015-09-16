---
title: 'initFocusEvent'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/FocusEvent
    href: /dom/FocusEvent
standardization_status: 'W3C Working Draft'
summary: 'Initializes a new FocusEvent that the  createEvent method created.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/FocusEvent/initFocusEvent

---
## Summary

Initializes a new FocusEvent that the createEvent method created.

Method of [dom/FocusEvent](/dom/FocusEvent)[dom/FocusEvent](/dom/FocusEvent)

## Syntax

``` js
 event.initFocusEvent(eventType, canBubble, cancelable, view, detail, relatedTarget);
```

## Parameters

### eventType

 Data-type
:   String

 The name of the event. Sets the value for the [**type**](/dom/Event/type) property.

### canBubble

 Data-type
:   Boolean

 Whether the event propagates upward. Sets the value for the [bubbles](/dom/Event/bubbles) property.

### cancelable

 Data-type
:   Boolean

 Whether the event is cancelable and so [preventDefault](/dom/Event/preventDefault) can be called. Sets the value for the [cancelable](/dom/Event/cancelable) property.

### view

 Data-type
:   Object

 The window on which this event is occurring. Sets the value for the [view](/dom/UIEvent/view) property.

### detail

 Data-type
:   Number

 Specifies additional information. This value is returned in the [**detail**](/dom/UIEvent/detail) property of the event.

### relatedTarget

 Data-type
:   DOM Node

 A secondary element that is involved in the event. This value is returned in the [**relatedTarget**](/dom/MouseEvent/relatedTarget) property of the event.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Related specifications

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## See also

### Related pages

-   FocusEvent[FocusEvent](/dom/FocusEvent)
-   initUIEvent[initUIEvent](/dom/UIEvent/initUIEvent)
