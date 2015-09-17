---
title: 'elapsedTime'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs spec reference, standardization status'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/AnimationEvent
    href: /dom/AnimationEvent
summary: 'The amount of time the animation has been running, in seconds, since the event fired, excluding any time the animation was paused.'
tags:
  - API_Object_Properties
  - DOM
uri: dom/AnimationEvent/elapsedTime

---
## Summary

The amount of time the animation has been running, in seconds, since the event fired, excluding any time the animation was paused.

Property of [dom/AnimationEvent](/dom/AnimationEvent)[dom/AnimationEvent](/dom/AnimationEvent)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.elapsedTime;
```

## Examples

``` js
//for a predefined animation event that is running
var myAnimEvent = new AnimationEvent();
// . . .
//retrieve the elapased time
var myAnimTime = myAnimEvent.elapsedTime;
```

## Notes

For an **animationstart** event, the elapsedTime is zero (0.0) unless there was a negative value for *animation-delay*, in which case the event will be fired with an elapsedTime of *(-1 \* delay)*.
