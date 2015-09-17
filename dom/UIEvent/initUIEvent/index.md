---
title: 'initUIEvent'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[event.initUIEvent](https://developer.mozilla.org/en-US/docs/Web/API/event.initUIEvent) Article]'
  - 'Microsoft Developer Network: [[initUIEvent Method](http://msdn.microsoft.com/en-us/library/ie/ff975256(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/UIEvent
    href: /dom/UIEvent
standardization_status: 'W3C Working Draft'
summary: 'Initializes a new user interface event that the  createEvent method created.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/UIEvent/initUIEvent

---
## Summary

Initializes a new user interface event that the createEvent method created.

Method of [dom/UIEvent](/dom/UIEvent)[dom/UIEvent](/dom/UIEvent)

## Syntax

``` js
 event.initUIEvent(/* see parameter list */);
```

## Parameters

### eventType

 Data-type
:   String

 The name of the event. Sets the value for the [type](/dom/Event/type) property. valid values are:

abort - An onabort event. error - An onerror event. load - An onload event. select - An onselect event. resize - An onresize event.

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
:   DOM Node

 The window on which this event is occurring. Sets the value for the [view](/dom/UIEvent/view) property.

### detail

 Data-type
:   Number

 Specifies additional information. This value is returned in the [detail](/dom/UIEvent/detail) property of the event.

## Return Value

No return value

## Examples

``` js
var evt = document.createEvent("UIEvents");
// creates a click event that bubbles, can be cancelled,
// and with its view and detail property initialized to window and 1,
// respectively
evt.initUIEvent("click", true, true, window, 1);
```

## Related specifications

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft
