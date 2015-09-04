---
title: elapsedTime
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
notes:
  - 'Needs spec reference, standardization status'
summary: 'The amount of time the animation has been running, in seconds, since the event fired, excluding any time the animation was paused.'
uri: dom/AnimationEvent/elapsedTime

---
# elapsedTime

## Summary

The amount of time the animation has been running, in seconds, since the event fired, excluding any time the animation was paused.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/AnimationEvent](/dom/AnimationEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.elapsedTime;
```

## Examples

``` {.js}
//for a predefined animation event that is running
var myAnimEvent = new AnimationEvent();
// . . .
//retrieve the elapased time
var myAnimTime = myAnimEvent.elapsedTime;
```

## Notes

For an **animationstart** event, the elapsedTime is zero (0.0) unless there was a negative value for *animation-delay*, in which case the event will be fired with an elapsedTime of *(-1 \* delay)*.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

