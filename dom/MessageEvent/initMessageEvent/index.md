---
title: initMessageEvent
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
notes:
  - 'example, standards, compatibility'
summary: 'Initializes a new cross-document message (XDM) event  that the  createEvent method created.'
uri: dom/MessageEvent/initMessageEvent

---
# initMessageEvent

## Summary

Initializes a new cross-document message (XDM) event that the createEvent method created.

*Method of [dom/MessageEvent](/dom/MessageEvent)*

## Syntax

``` {.js}
 event.initMessageEvent(eventType, canBubble, cancelable, data, origin, lastEventId, source);
```

## Parameters

### eventType

 Data-typeÂ
:   String

 The name of the event. Sets the value for the [**type**](/dom/Event/type) property.

### canBubble

 Data-typeÂ
:   Boolean

 Whether the event propagates upward. Sets the value for the [bubbles](/dom/Event/bubbles) property.

### cancelable

 Data-typeÂ
:   Boolean

 Whether the event is cancelable and so [preventDefault](/dom/Event/preventDefault) can be called. Sets the value for the [cancelable](/dom/Event/cancelable) property.

### data

 Data-typeÂ
:   any

 The cross-document message. Sets the value for the [**data**](/dom/MessageEvent/data) property.

### origin

 Data-typeÂ
:   String

 The originating domain of the message. Sets the value for the [**origin**](/dom/MessageEvent/origin) property.

### lastEventId

 Data-typeÂ
:   String

 Not used. Set this parameter to an empty string.

### source

 Data-typeÂ
:   Object

 A reference to the **window** that generated the event. Sets the value for the [**source**](/dom/MessageEvent/source) property.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft
[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage/)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

