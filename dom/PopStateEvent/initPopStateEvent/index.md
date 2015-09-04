---
title: initPopStateEvent
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Initializes the properties of a PopStateEvent.'
uri: dom/PopStateEvent/initPopStateEvent

---
# initPopStateEvent

## Summary

Initializes the properties of a PopStateEvent.

*Method of [dom/PopStateEvent](/dom/PopStateEvent)*

## Syntax

``` {.js}
var object = object.initPopStateEvent(/* see parameter list */);
```

## Parameters

### typeArg

 Data-typeÂ
:   any

 The type of the event being created.

### canBubbleArg

 Data-typeÂ
:   any

 Indicates whether the event can bubble. When true, the event propagates upward. When false, the event does not propagate upward.

### cancelableArg

 Data-typeÂ
:   Boolean

 Indicates whether the eventâ€™s default action can be prevented. When true, the default action can be canceled. When false, the default action cannot be canceled.

### stateArg

 Data-typeÂ
:   any

 The object to be applied to the [**state**](/dom/PopStateEvent/state) property.

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

This method can return one of these values.

S\_OK

## Examples

``` {.js}
var evt = document.createEvent("PopStateEvent");
evt.initPopStateEvent("popstate", false, false, { .. state object  ..});
window.dispatchEvent(evt);
```

## Notes

### Remarks

Initializes attributes of an event created through the [**createEvent**](/dom/Document/createEvent) method. This method can only be called before the event has been dispatched via the [**dispatchEvent**](/dom/EventTarget/dispatchEvent) method. If the method is called several times before invoking **dispatchEvent**, only the final invocation takes precedence. This method has no effect if called after the event has been dispatched.

### Syntax

var retval = PopStateEvent.initPopStateEvent(typeArg, canBubbleArg, cancelableArg, stateArg);

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[initPopStateEvent Method](http://msdn.microsoft.com/en-us/library/ie/hh772350(v=vs.85).aspx) Article]

