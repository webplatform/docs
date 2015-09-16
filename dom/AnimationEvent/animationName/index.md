---
title: 'animationName'
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
summary: 'The value of the animation-name property of the animation that fired the animation event.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/AnimationEvent/animationName

---
## Summary

The value of the animation-name property of the animation that fired the animation event.

Property of [dom/AnimationEvent](/dom/AnimationEvent)[dom/AnimationEvent](/dom/AnimationEvent)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.animationName;
```

## Examples

``` js
//define animation event
var myAnimEvent = new AnimationEvent();
//retrieve name
var myAnimName = myAnimEvent.animationName;
```

