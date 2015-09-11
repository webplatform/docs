---
title: initUIEvent
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
  - API
  - Object
  - Methods
  - DOM
uri: dom/UIEvent/initUIEvent

---
## <span>Summary</span>

Initializes a new user interface event that the createEvent method created.

Method of [dom/UIEvent](/dom/UIEvent)[dom/UIEvent](/dom/UIEvent)

## <span>Syntax</span>

``` js
 event.initUIEvent(/* see parameter list */);
```

## <span>Parameters</span>

### <span>eventType</span>

 Data-type
:   String

 The name of the event. Sets the value for the [type](/dom/Event/type) property. valid values are:

abort - An onabort event. error - An onerror event. load - An onload event. select - An onselect event. resize - An onresize event.

### <span>canBubble</span>

 Data-type
:   Boolean

 Whether the event propagates upward. Sets the value for the [bubbles](/dom/Event/bubbles) property.

### <span>cancelable</span>

 Data-type
:   Boolean

 Whether the event is cancelable and so [preventDefault](/dom/Event/preventDefault) can be called. Sets the value for the [cancelable](/dom/Event/cancelable) property.

### <span>view</span>

 Data-type
:   DOM Node

 The window on which this event is occurring. Sets the value for the [view](/dom/UIEvent/view) property.

### <span>detail</span>

 Data-type
:   Number

 Specifies additional information. This value is returned in the [detail](/dom/UIEvent/detail) property of the event.

## <span>Return Value</span>

No return value

## <span>Examples</span>

``` js
var evt = document.createEvent("UIEvents");
// creates a click event that bubbles, can be cancelled,
// and with its view and detail property initialized to window and 1,
// respectively
evt.initUIEvent("click", true, true, window, 1);
```

## <span>Related specifications</span>

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft
