---
title: composite
tags:
  - API
  - Object
  - Properties
  - Web
  - Animations
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
summary: 'The possible values of an animation effect''s composition behavior are represented by the CompositeOperation enumeration.'
uri: 'apis/web animations/AnimationEffect/composite'

---
# composite

## Summary

The possible values of an animation effect's composition behavior are represented by the CompositeOperation enumeration.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/web\_animations/AnimationEffect](/apis/web_animations/AnimationEffect)</span></span>

## Syntax

``` {.js}
var result = element.composite;
element.composite = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Object</span></span>

Returns a CompositeOperation object, specified by the CompositeOperation enumeration.

Possible values are replace, add, accumulate.

---

replace Corresponds to the replace composite operation value such that the animation effect overrides the underlying value it is combined with.

add Corresponds to the add composite operation value such that the animation effect is added to the underlying value with which it is combined.

accumulate Corresponds to the accumulate composite operation value such that the animation effect is accumulated on to the underlying value.

**Needs Examples**: This section should include examples.

