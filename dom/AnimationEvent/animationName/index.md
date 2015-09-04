---
title: animationName
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
notes:
  - 'Needs spec reference, standardization status'
summary: 'The value of the animation-name property of the animation that fired the animation event.'
uri: dom/AnimationEvent/animationName

---
# animationName

## Summary

The value of the animation-name property of the animation that fired the animation event.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/AnimationEvent](/dom/AnimationEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.animationName;
```

## Examples

``` {.js}
//define animation event
var myAnimEvent = new AnimationEvent();
//retrieve name
var myAnimName = myAnimEvent.animationName;
```

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

