---
title: initDragEvent
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs examples and compat'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/DragEvent
    href: /dom/DragEvent
standardization_status: 'W3C Candidate Recommendation'
summary: 'Initializes a new drag event.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/DragEvent/initDragEvent

---
## Summary

Initializes a new drag event.

Method of [dom/DragEvent](/dom/DragEvent)[dom/DragEvent](/dom/DragEvent)

## Syntax

``` js
 event.initDragEvent(eventType, canBubble, cancelable, view, detail, screenX, screenY, clientY, ctrlKey, altKey, shiftKey, metaKey, button, relatedTarget, dataTransfer);
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
:   String

 Whether the event is cancelable and so [preventDefault](/dom/Event/preventDefault) can be called. Sets the value for the [cancelable](/dom/Event/cancelable) property.

### view

 Data-type
:   DOM Node

 The window on which this event is occurring. Sets the value for the [view](/dom/UIEvent/view) property.

### detail

 Data-type
:   Number

 Specifies additional information. This value is returned in the [**detail**](/dom/UIEvent/detail) property of the event.

### screenX

 Data-type
:   Number

 The x-coordinate of the mouse pointer, relative to the upper-left corner of the screen. This value is returned in the [**screenX**](/dom/MouseEvent/screenX) property of the event.

### screenY

 Data-type
:   Number

 The y-coordinate of the mouse pointer, relative to the upper-left corner of the screen. This value is returned in the [**screenY**](/dom/MouseEvent/screenY) property of the event.

### clientX

 Data-type
:   Number

 The x-coordinate of the mouse pointer, relative to the upper-left corner of the browser's client area. This value is returned in the [**clientX**](/dom/MouseEvent/clientX) property of the event.

### clientY

 Data-type
:   Number

 The y-coordinate of the mouse pointer, relative to the upper-left corner of the browser's client area. This value is returned in the [**clientY**](/dom/MouseEvent/clientY) property of the event.

### ctrlKey

 Data-type
:   Boolean

 The value that is returned in the [**ctrlKey**](/dom/KeyboardEvent/ctrlKey) property of the event.

### altKey

 Data-type
:   Boolean

 The value that is returned in the [**altKey**](/dom/KeyboardEvent/altKey) property of the event.

### shiftKey

 Data-type
:   Boolean

 The value that is returned in the [**shiftKey**](/dom/KeyboardEvent/shiftKey) property of the event.

### metaKey

 Data-type
:   Boolean

 The value that is returned in the [**metaKey**](/dom/KeyboardEvent/metaKey) property of the event.

### button

 Data-type
:   Number

 The mouse button that caused the event. This value is returned in the [**button**](/dom/MouseEvent/button) property of the event.

### relatedTarget

 Data-type
:   DOM Node

 A secondary element that is involved in the event. This value is returned in the [**relatedTarget**](/dom/MouseEvent/relatedTarget) property of the event.

### dataTransfer

 Data-type
:   String

 A [DataTransfer](/dom/DataTransfer) object.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Related specifications

[HTML5](http://www.w3.org/TR/html5/)
:   Working Draft
