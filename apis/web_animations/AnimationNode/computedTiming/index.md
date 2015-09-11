---
title: computedTiming
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/web_animations/AnimationNode
    href: /apis/web_animations/AnimationNode
  return:
    predicate: 'Returns an object of type '
    value: Object
    href: /apis/web_animations/AnimationNode
standardization_status: 'W3C Editor''s Draft'
summary: "Returns the calculated timing properties for this animation node. This is comparable to the computed style of an Element, window.getComputedStyle(elem).\n"
tags:
  - API
  - Object
  - Properties
  - Web
  - Animations
uri: 'apis/web animations/AnimationNode/computedTiming'

---
## <span>Summary</span>

Returns the calculated timing properties for this animation node. This is comparable to the computed style of an Element, window.getComputedStyle(elem).

Although several of the attributes of the this object are common to the AnimationTiming object returned by the timing attribute, they have the following differences:

duration – returns the calculated value of the iteration duration. If timing.duration is the string auto or any unsupported value, this attribute will return the current calculated value of the intrinsic iteration duration. fill – the auto value is replaced with the specific FillMode depending on the type of animation node (see §5.8.1 The FillMode enumeration). easing – unrecognised or unsupported values are replaced with the string linear.

Property of [apis/web\_animations/AnimationNode](/apis/web_animations/AnimationNode)[apis/web\_animations/AnimationNode](/apis/web_animations/AnimationNode)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = element.computedTiming;
```

## <span>Return Value</span>

Returns an object of type ObjectObject

returns a ComputedTimingProperties object.

**Needs Examples**: This section should include examples.

