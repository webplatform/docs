---
title: removeEventListener
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
standardization_status: 'W3C Recommendation'
summary: 'Removes an event handler that the addEventListener method registered.'
tags:
  - API
  - Object
  - Methods
  - DOM
  - DOMEvents
uri: dom/EventTarget/removeEventListener

---
## <span>Summary</span>

Removes an event handler that the addEventListener method registered.

Method of [dom/EventTarget](/dom/EventTarget)[dom/EventTarget](/dom/EventTarget)

## <span>Syntax</span>

``` js
 target.removeEventListener(type, listener, useCapture);
```

## <span>Parameters</span>

### <span>type</span>

 Data-type
:   String

 The event [**type**](/dom/Event/type) that the event handler is registered for.

### <span>listener</span>

 Data-type
:   function

 The event handler function to remove.

### <span>useCapture</span>

 Data-type
:   Boolean

 A **Boolean** value that specifies the event phase to remove the event handler from.

## <span>Return Value</span>

No return value

**Needs Examples**: This section should include examples.

## <span>Notes</span>

If you register multiple identical event handlers for the same event type, the duplicate event handlers are discarded. You can remove only the first instance. If the arguments for **removeEventListener** do not identify a registered event handler, the call to **removeEventListener** has no effect.

## <span>Related specifications</span>

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft
