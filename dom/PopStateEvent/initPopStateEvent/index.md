---
title: initPopStateEvent
attributions:
  - 'Microsoft Developer Network: [[initPopStateEvent Method](http://msdn.microsoft.com/en-us/library/ie/hh772350(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/PopStateEvent
    href: /dom/PopStateEvent
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/PopStateEvent
standardization_status: 'W3C Recommendation'
summary: 'Initializes the properties of a PopStateEvent.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/PopStateEvent/initPopStateEvent

---
## <span>Summary</span>

Initializes the properties of a PopStateEvent.

Method of [dom/PopStateEvent](/dom/PopStateEvent)[dom/PopStateEvent](/dom/PopStateEvent)

## <span>Syntax</span>

``` js
var object = object.initPopStateEvent(/* see parameter list */);
```

## <span>Parameters</span>

### <span>typeArg</span>

 Data-type
:   any

 The type of the event being created.

### <span>canBubbleArg</span>

 Data-type
:   any

 Indicates whether the event can bubble. When true, the event propagates upward. When false, the event does not propagate upward.

### <span>cancelableArg</span>

 Data-type
:   Boolean

 Indicates whether the event’s default action can be prevented. When true, the default action can be canceled. When false, the default action cannot be canceled.

### <span>stateArg</span>

 Data-type
:   any

 The object to be applied to the [**state**](/dom/PopStateEvent/state) property.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

This method can return one of these values.

S\_OK

## <span>Examples</span>

``` js
var evt = document.createEvent("PopStateEvent");
evt.initPopStateEvent("popstate", false, false, { .. state object  ..});
window.dispatchEvent(evt);
```

## <span>Notes</span>

### <span>Remarks</span>

Initializes attributes of an event created through the [**createEvent**](/dom/Document/createEvent) method. This method can only be called before the event has been dispatched via the [**dispatchEvent**](/dom/EventTarget/dispatchEvent) method. If the method is called several times before invoking **dispatchEvent**, only the final invocation takes precedence. This method has no effect if called after the event has been dispatched.

### <span>Syntax</span>

var retval = PopStateEvent.initPopStateEvent(typeArg, canBubbleArg, cancelableArg, stateArg);