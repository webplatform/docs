---
title: 'timing'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/web_animations/AnimationNode
    href: /apis/web_animations/AnimationNode
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /apis/web_animations/AnimationNode
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the input timing properties specified for this animation node. This is comparable to the specified style on an Element, elem.style.'
tags:
  - API
  - Object
  - Properties
  - Web
  - Animations
uri: 'apis/web animations/AnimationNode/timing'

---
## Summary

Returns the input timing properties specified for this animation node. This is comparable to the specified style on an Element, elem.style.

Property of [apis/web\_animations/AnimationNode](/apis/web_animations/AnimationNode)[apis/web\_animations/AnimationNode](/apis/web_animations/AnimationNode)

## Syntax

**Note**: This property is read-only.

``` js
var myTiming = myAnimationNode.timing;
```

## Return Value

Returns an object of type

type AnimationTiming object

**Needs Examples**: This section should include examples.

## See also

### Related articles

#### Animation

-   [Web Animations API](/apis/web_animations)

-   [clone](/apis/web_animations/AnimationEffect/clone)

-   [AnimationNode](/apis/web_animations/AnimationNode)

-   **timing**

-   [currentTime](/apis/web_animations/AnimationPlayer/currentTime)

-   [reverse](/apis/web_animations/AnimationPlayer/reverse)

-   [source](/apis/web_animations/AnimationPlayer/source)

-   [AnimationPlayerEvent](/apis/web_animations/AnimationPlayerEvent)

-   [currentTime](/apis/web_animations/AnimationTimeline/currentTime)

-   [play](/apis/web_animations/AnimationTimeline/play)

-   [@keyframes](/css/atrules/@keyframes)

-   [CSSKeyframeRule](/css/cssom/CSSKeyframeRule)

-   [keyText](/css/cssom/CSSKeyframeRule/keyText)

-   [style](/css/cssom/CSSKeyframeRule/style)

-   [CSSKeyframesRule](/css/cssom/CSSKeyframesRule)

-   [cssRules](/css/cssom/CSSKeyframesRule/cssRules)

-   [deleteRule](/css/cssom/CSSKeyframesRule/deleteRule)

-   [findRule](/css/cssom/CSSKeyframesRule/findRule)

-   [insertRule](/css/cssom/CSSKeyframesRule/insertRule)

-   [name](/css/cssom/CSSKeyframesRule/name)

-   [cubic-bezier](/css/functions/cubic-bezier)

-   [Animations](/css/properties/animations)

-   [transition](/css/properties/transition)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)
