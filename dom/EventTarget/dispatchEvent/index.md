---
title: dispatchEvent
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/EventTarget
    href: /dom/EventTarget
  return_type:
    predicate: 'Returns an object of type  '
    value: Boolean
    href: /dom/EventTarget
standardization_status: 'W3C Recommendation'
summary: 'Sends an event to the current element.'
tags:
  - API
  - Object
  - Methods
  - DOM
  - DOMEvents
uri: dom/EventTarget/dispatchEvent

---
## <span>Summary</span>

Sends an event to the current element.

Method of [dom/EventTarget](/dom/EventTarget)[dom/EventTarget](/dom/EventTarget)

## <span>Syntax</span>

``` js
var defaultPrevented = eventTarget.dispatchEvent(event);
```

## <span>Parameters</span>

### <span>event</span>

 Data-type
:   String

 The event object to dispatch.

## <span>Return Value</span>

Returns an object of type BooleanBoolean

Whether any of the event handlers called [**preventDefault**](/dom/Event/preventDefault).

Default. The default action is permitted.

The caller should prevent the default action.

**Needs Examples**: This section should include examples.

## <span>Notes</span>

Events that the **dispatchEvent** method dispatches are subject to the same capturing and bubbling behavior as events that the browser dispatches. You cannot cancel some events. For more information, see the documentation for the event.

## <span>Related specifications</span>

[DOM Level 2 Events](http://www.w3.org/TR/DOM-Level-2-Events/)
:   Recommendation
