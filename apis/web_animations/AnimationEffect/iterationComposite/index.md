---
title: iterationComposite
tags:
  - API
  - Object
  - Properties
  - Web
  - Animations
readiness: 'Almost Ready'
standardization_status: 'W3C Editor''s Draft'
summary: 'The iteration composite operation property of this animation effect as specified by one of the IterationCompositeOperation enumeration values.'
uri: 'apis/web animations/AnimationEffect/iterationComposite'

---
# iterationComposite

## Summary

The iteration composite operation property of this animation effect as specified by one of the IterationCompositeOperation enumeration values.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/web\_animations/AnimationEffect](/apis/web_animations/AnimationEffect)</span></span>

## Syntax

``` {.js}
var result = element.iterationComposite;
element.iterationComposite = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Object</span></span>

Returns an IterationCompositeOperation enumerations object.

Current values are either:

replace Corresponds to the replace iteration composite operation value such that the intermediate animation value produced is independent of the current iteration.

accumulate Corresponds to the accumulate iteration composite operation value such that subsequent iterations of an animation build on the final value of the previous iteration.

**Needs Examples**: This section should include examples.

