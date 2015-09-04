---
title: dispatchEvent
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
summary: 'Sends an event to the current element.'
uri: dom/EventTarget/dispatchEvent

---
# dispatchEvent

## Summary

Sends an event to the current element.

*Method of [dom/EventTarget](/dom/EventTarget)*

## Syntax

``` {.js}
var defaultPrevented = eventTarget.dispatchEvent(event);
```

## Parameters

### event

 Data-typeÂ
:   String

 The event object to dispatch.

## Return Value

Returns an object of type Boolean.

Whether any of the event handlers called [**preventDefault**](/dom/Event/preventDefault).

Default. The default action is permitted.

The caller should prevent the default action.

**Needs Examples**: This section should include examples.

## Notes

Events that the **dispatchEvent** method dispatches are subject to the same capturing and bubbling behavior as events that the browser dispatches. You cannot cancel some events. For more information, see the documentation for the event.

## Related specifications

Specification
:   Status
[DOM Level 2 Events](http://www.w3.org/TR/DOM-Level-2-Events/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

