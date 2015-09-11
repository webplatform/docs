---
title: composite
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
  - API
  - Object
  - Properties
  - Web
  - Animations
uri: 'apis/web animations/AnimationEffect/composite'

---
## <span>Summary</span>

The possible values of an animation effect's composition behavior are represented by the CompositeOperation enumeration.

Property of [apis/web\_animations/AnimationEffect](/apis/web_animations/AnimationEffect)[apis/web\_animations/AnimationEffect](/apis/web_animations/AnimationEffect)

## <span>Syntax</span>

``` js
var result = element.composite;
element.composite = value;
```

## <span>Return Value</span>

Returns an object of type ObjectObject

Returns a CompositeOperation object, specified by the CompositeOperation enumeration.

Possible values are replace, add, accumulate.

---

replace Corresponds to the replace composite operation value such that the animation effect overrides the underlying value it is combined with.

add Corresponds to the add composite operation value such that the animation effect is added to the underlying value with which it is combined.

accumulate Corresponds to the accumulate composite operation value such that the animation effect is accumulated on to the underlying value.

**Needs Examples**: This section should include examples.

