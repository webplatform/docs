---
title: CompositeOperation
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
summary: 'The possible values of an animation effect''s composition behavior are represented by the CompositeOperation enumeration.'
tags:
  - Constants
  - Web
  - Animations
uri: 'apis/web animations/AnimationEffect/CompositeOperation'

---
## Summary

The possible values of an animation effect's composition behavior are represented by the CompositeOperation enumeration.

 enum CompositeOperation { "replace", "add", "accumulate" };

 replace Corresponds to the replace composite operation value such that the animation effect overrides the underlying value it is combined with. add Corresponds to the add composite operation value such that the animation effect is added to the underlying value with which it is combined. accumulate Corresponds to the accumulate composite operation value such that the animation effect is accumulated on to the underlying value.

**Needs Examples**: This section should include examples.

