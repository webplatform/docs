---
title: 'initMessageEvent'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'example, standards, compatibility'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/MessageEvent
    href: /dom/MessageEvent
standardization_status: 'W3C Working Draft'
summary: 'Initializes a new cross-document message (XDM) event  that the  createEvent method created.'
tags:
  - API_Object_Methods
  - DOM
  - Needs_Examples
uri: dom/MessageEvent/initMessageEvent

---
## Summary

Initializes a new cross-document message (XDM) event that the createEvent method created.

Method of [dom/MessageEvent](/dom/MessageEvent)[dom/MessageEvent](/dom/MessageEvent)

## Syntax

``` js
 event.initMessageEvent(eventType, canBubble, cancelable, data, origin, lastEventId, source);
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

### data

 Data-type
:   any

 The cross-document message. Sets the value for the [**data**](/dom/MessageEvent/data) property.

### origin

 Data-type
:   String

 The originating domain of the message. Sets the value for the [**origin**](/dom/MessageEvent/origin) property.

### lastEventId

 Data-type
:   String

 Not used. Set this parameter to an empty string.

### source

 Data-type
:   Object

 A reference to the **window** that generated the event. Sets the value for the [**source**](/dom/MessageEvent/source) property.

## Return Value

No return value

## Related specifications

[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage/)
:   Living Standard
