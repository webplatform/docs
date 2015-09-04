---
title: removeEventListener
tags:
  - API
  - Object
  - Methods
  - DOM
  - DOMEvents
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs example'
summary: 'Removes an event handler that the addEventListener method registered.'
uri: dom/EventTarget/removeEventListener

---
# removeEventListener

## Summary

Removes an event handler that the addEventListener method registered.

*Method of [dom/EventTarget](/dom/EventTarget)*

## Syntax

``` {.js}
 target.removeEventListener(type, listener, useCapture);
```

## Parameters

### type

 Data-typeÂ
:   String

 The event [**type**](/dom/Event/type) that the event handler is registered for.

### listener

 Data-typeÂ
:   function

 The event handler function to remove.

### useCapture

 Data-typeÂ
:   Boolean

 A **Boolean** value that specifies the event phase to remove the event handler from.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Notes

If you register multiple identical event handlers for the same event type, the duplicate event handlers are discarded. You can remove only the first instance. If the arguments for **removeEventListener** do not identify a registered event handler, the call to **removeEventListener** has no effect.

## Related specifications

Specification
:   Status
[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

