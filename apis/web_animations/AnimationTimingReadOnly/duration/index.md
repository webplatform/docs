---
title: 'duration'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/web_animations/AnimationTimingReadOnly
    href: /apis/web_animations/AnimationTimingReadOnly
  return:
    predicate: 'Returns an object of type '
    value: Object
    href: /apis/web_animations/AnimationTimingReadOnly
standardization_status: 'W3C Editor''s Draft'
summary: "The iteration duration which is a real number greater than or equal to zero (including positive infinity) representing the time taken to complete a single iteration of the animation node.\n"
tags:
  - API
  - Object
  - Properties
  - Web
  - Animations
uri: 'apis/web animations/AnimationTimingReadOnly/duration'

---
## Summary

The iteration duration which is a real number greater than or equal to zero (including positive infinity) representing the time taken to complete a single iteration of the animation node.

Property of [apis/web\_animations/AnimationTimingReadOnly](/apis/web_animations/AnimationTimingReadOnly)[apis/web\_animations/AnimationTimingReadOnly](/apis/web_animations/AnimationTimingReadOnly)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.duration;
```

## Return Value

Returns an object of type ObjectObject

Returns and unrestricted double or DOMString object

The string value auto is used to indicate that the iteration duration reflects the animation node’s intrinsic iteration duration.

**Needs Examples**: This section should include examples.

