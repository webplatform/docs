---
title: initMessageEvent
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
  - API
  - Object
  - Methods
  - DOM
uri: dom/MessageEvent/initMessageEvent

---
## <span>Summary</span>

Initializes a new cross-document message (XDM) event that the createEvent method created.

Method of [dom/MessageEvent](/dom/MessageEvent)[dom/MessageEvent](/dom/MessageEvent)

## <span>Syntax</span>

``` js
 event.initMessageEvent(eventType, canBubble, cancelable, data, origin, lastEventId, source);
```

## <span>Parameters</span>

### <span>eventType</span>

 Data-type
:   String

 The name of the event. Sets the value for the [**type**](/dom/Event/type) property.

### <span>canBubble</span>

 Data-type
:   Boolean

 Whether the event propagates upward. Sets the value for the [bubbles](/dom/Event/bubbles) property.

### <span>cancelable</span>

 Data-type
:   Boolean

 Whether the event is cancelable and so [preventDefault](/dom/Event/preventDefault) can be called. Sets the value for the [cancelable](/dom/Event/cancelable) property.

### <span>data</span>

 Data-type
:   any

 The cross-document message. Sets the value for the [**data**](/dom/MessageEvent/data) property.

### <span>origin</span>

 Data-type
:   String

 The originating domain of the message. Sets the value for the [**origin**](/dom/MessageEvent/origin) property.

### <span>lastEventId</span>

 Data-type
:   String

 Not used. Set this parameter to an empty string.

### <span>source</span>

 Data-type
:   Object

 A reference to the **window** that generated the event. Sets the value for the [**source**](/dom/MessageEvent/source) property.

## <span>Return Value</span>

No return value

**Needs Examples**: This section should include examples.

## <span>Related specifications</span>

[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage/)
:   Living Standard
