---
title: 'iterationComposite'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/web_animations/AnimationEffect
    href: /apis/web_animations/AnimationEffect
  return:
    predicate: 'Returns an object of type '
    value: Object
    href: /apis/web_animations/AnimationEffect
standardization_status: 'W3C Editor''s Draft'
summary: 'The iteration composite operation property of this animation effect as specified by one of the IterationCompositeOperation enumeration values.'
tags:
  - API_Object_Properties
  - Web_Animations
  - Needs_Examples
uri: 'apis/web animations/AnimationEffect/iterationComposite'

---
## Summary

The iteration composite operation property of this animation effect as specified by one of the IterationCompositeOperation enumeration values.

Property of [apis/web\_animations/AnimationEffect](/apis/web_animations/AnimationEffect)[apis/web\_animations/AnimationEffect](/apis/web_animations/AnimationEffect)

## Syntax

``` js
var result = element.iterationComposite;
element.iterationComposite = value;
```

## Return Value

Returns an object of type ObjectObject

Returns an IterationCompositeOperation enumerations object.

Current values are either:

replace Corresponds to the replace iteration composite operation value such that the intermediate animation value produced is independent of the current iteration.

accumulate Corresponds to the accumulate iteration composite operation value such that subsequent iterations of an animation build on the final value of the previous iteration.

