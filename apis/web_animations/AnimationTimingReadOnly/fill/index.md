---
title: fill
readiness: 'In Progress'
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
summary: "The fill mode as specified by one of the FillMode enumeration values.\n"
tags:
  - API
  - Object
  - Properties
  - Web
  - Animations
uri: 'apis/web animations/AnimationTimingReadOnly/fill'

---
## <span>Summary</span>

The fill mode as specified by one of the FillMode enumeration values.

When performing timing calculations the special value auto is expanded to one of the fill modes recognized by the timing model as follows,

If the animation node to which the fill mode is being is applied is an animation, Use none as the fill mode. Otherwise, Use both as the fill mode.

Property of [apis/web\_animations/AnimationTimingReadOnly](/apis/web_animations/AnimationTimingReadOnly)[apis/web\_animations/AnimationTimingReadOnly](/apis/web_animations/AnimationTimingReadOnly)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = element.fill;
```

## <span>Return Value</span>

Returns an object of type ObjectObject

Returns a FillMode object

**Needs Examples**: This section should include examples.

