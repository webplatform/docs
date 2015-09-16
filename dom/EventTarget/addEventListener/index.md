---
title: addEventListener
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/EventTarget
    href: /dom/EventTarget
standardization_status: 'W3C Recommendation'
summary: 'Registers an event handler for the specified event type.'
tags:
  - API
  - Object
  - Methods
  - DOM
  - DOMEvents
uri: dom/EventTarget/addEventListener

---
## Summary

Registers an event handler for the specified event type.

Method of [dom/EventTarget](/dom/EventTarget)[dom/EventTarget](/dom/EventTarget)

## Syntax

``` js
 target.addEventListener(type, handler, useCapture);
```

## Parameters

### type

 Data-type
:   String

 The type of event [**type**](/dom/Event/type) to register.

### handler

 Data-type
:   function

 A **function** that is called when the event is fired.

### useCapture

 Data-type
:   Boolean

(Optional)

A **Boolean** value that specifies the event phase to add the event handler for.

While this parameter is officially optional, it may only be omitted in modern browsers.

## Return Value

No return value

## Examples

This example listens to any click events on the document or its descendants.

``` js
document.addEventListener(
  "click",
  function (e) {
    console.log("A " + e.type + " event was fired.");
  },
  false);
```

## Notes

1.  Events are handled in two phases: capturing and bubbling. During the capturing phase, events are dispatched to parent objects before they are dispatched to event targets that are lower in the object hierarchy. During the bubbling phase, events are dispatched to target elements first and then to parent elements. You can register event handlers for either event phase. For more information, see [**eventPhase**](/dom/Event/eventPhase).
2.  Some events, such as [**onfocus**](/dom/HTMLElement/focus), do not bubble. However, you can capture all events. You cannot capture events by elements that are not parents of the target element.
3.  If you register multiple identical event handlers on the same event target, the duplicate event handlers are discarded.

## Related specifications

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft
