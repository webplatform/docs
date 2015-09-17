---
title: 'composite'
readiness: 'In Progress'
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
summary: 'The possible values of an animation effect''s composition behavior are represented by the CompositeOperation enumeration.'
tags:
  - API_Object_Properties
  - Web_Animations
  - Needs_Examples
uri: 'apis/web animations/AnimationEffect/composite'

---
## Summary

The possible values of an animation effect's composition behavior are represented by the CompositeOperation enumeration.

Property of [apis/web\_animations/AnimationEffect](/apis/web_animations/AnimationEffect)[apis/web\_animations/AnimationEffect](/apis/web_animations/AnimationEffect)

## Syntax

``` js
var result = element.composite;
element.composite = value;
```

## Return Value

Returns an object of type ObjectObject

Returns a CompositeOperation object, specified by the CompositeOperation enumeration.

Possible values are replace, add, accumulate.

---

replace Corresponds to the replace composite operation value such that the animation effect overrides the underlying value it is combined with.

add Corresponds to the add composite operation value such that the animation effect is added to the underlying value with which it is combined.

accumulate Corresponds to the accumulate composite operation value such that the animation effect is accumulated on to the underlying value.

