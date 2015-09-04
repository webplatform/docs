---
title: iterationStart
tags:
  - API
  - Object
  - Properties
readiness: readiness-state
summary: "See the iterationStart member of the AnimationTimingReadOnly interface.\n"
uri: 'apis/web animations/AnimationTimingProperties/iterationStart'

---
# iterationStart

## Summary

See the iterationStart member of the AnimationTimingReadOnly interface.

Values less than zero are clamped to zero for the purpose of timing model calculations.

Note that the value of iterations is effectively added to the iterationStart such that an animation node with an iterationStart of ‘0.5’ and iterations of ‘2’ would still repeat twice however it would begin and end half-way through the animation node’s iteration interval. Setting the iterationStart to a value greater than or equal to one is typically only useful in combination with an animation effect that has an iteration composite operation of ‘accumulate’.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/web animations/AnimationTimingProperties](/apis/web_animations/AnimationTimingProperties)</span></span>

## Syntax

``` {.js}
var result = element.iterationStart;
element.iterationStart = value;
```

**Needs Examples**: This section should include examples.

