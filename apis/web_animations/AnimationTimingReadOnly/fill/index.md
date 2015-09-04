---
title: fill
tags:
  - API
  - Object
  - Properties
  - Web
  - Animations
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
summary: "The fill mode as specified by one of the FillMode enumeration values.\n"
uri: 'apis/web animations/AnimationTimingReadOnly/fill'

---
# fill

## Summary

The fill mode as specified by one of the FillMode enumeration values.

When performing timing calculations the special value auto is expanded to one of the fill modes recognized by the timing model as follows,

If the animation node to which the fill mode is being is applied is an animation, Use none as the fill mode. Otherwise, Use both as the fill mode.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/web\_animations/AnimationTimingReadOnly](/apis/web_animations/AnimationTimingReadOnly)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.fill;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Object</span></span>

Returns a FillMode object

**Needs Examples**: This section should include examples.

