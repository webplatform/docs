---
title: 'initTransitionEvent'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[TransitionEvent.initTransitionEvent](https://developer.mozilla.org/en-US/docs/Web/API/TransitionEvent.initTransitionEvent) Article]'
  - 'Microsoft Developer Network: [[initTransitionEvent Method](http://msdn.microsoft.com/en-us/library/ie/hh772141(v=vs.85).aspx) Article]'
notes:
  - 'Not sure of the status of the standard. MDN says do not use....'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/TransitionEvent
    href: /dom/TransitionEvent
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/TransitionEvent
standardization_status: Deprecated
summary: 'Initializes a transition event created using the deprecated Document.createEvent(&quot;TransitionEvent&quot;) method.'
tags:
  - API_Object_Methods
  - DOM
  - Needs_Examples
uri: dom/TransitionEvent/initTransitionEvent

---
## Summary

Initializes a transition event created using the deprecated Document.createEvent(&quot;TransitionEvent&quot;) method.

Method of [dom/TransitionEvent](/dom/TransitionEvent)[dom/TransitionEvent](/dom/TransitionEvent)

## Syntax

``` js
var object = object.initTransitionEvent(/* see parameter list */);
```

## Parameters

### typeArg

 Data-type
:   any

 Specifies the event type.

### canBubbleArg

 Data-type
:   any

 Specifies whether or not the event can bubble.

### cancelableArg

 Data-type
:   any

 Specifies whether or not the event's default action can be prevented. Since a **TransitionEvent** is purely for notification, there is no default action.

### propertyNameArg

 Data-type
:   any

 Specifies the name of the property associated with the [**Event**](/dom/Event).

### elapsedTimeArg

 Data-type
:   any

 Specifies the amount of time, in seconds, the transition has been running at the time of initialization.

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

This method can return one of these values.

S\_OK

## Usage

     Used to initialize the value of a TransitionEvent.

Note: this method has been dropped during the standard process. It has been deprecated and is in the progress of been removed from most implementation. Do not use it anymore, use the standard constructor, TransitionEvent(), to create a synthetic TransitionEvent

## Notes

### Remarks

This method is used to initialize the value of a **TransitionEvent**. This method may only be called before the **TransitionEvent** has been dispatched via the [**dispatchEvent**](/dom/EventTarget/dispatchEvent) method, though it may be called multiple times during that phase if necessary. If called multiple times, the final invocation takes precedence.

### Syntax

var retval = transitionEvent.initTransitionEvent(typeArg, canBubbleArg, cancelableArg, propertyNameArg, elapsedTimeArg);
