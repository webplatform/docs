---
title: Web Animations API
notes:
  - 'API documentation needs to be competed.'
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
summary: 'Javascript programming interface for modeling synchronizing and timing the changes to a web page''s presentation.'
tags:
  0: API
  1: Listings
  3: Web
  4: Animations
uri: 'apis/web animations'

---
## <span>Summary</span>

Javascript programming interface for modeling synchronizing and timing the changes to a web page's presentation.

API Name
:   Summary

[Animatable](/apis/web_animations/Animatable)
:   Objects that may be the target of an [**Animation**](/apis/web_animations/Animation) implement the Animatable interface.

[AnimationGroup](/apis/web_animations/AnimationGroup)
:   Animation groups are represented by the AnimationGroup interface.

[AnimationNode](/apis/web_animations/AnimationNode)
:   Animation nodes are represented in the Web Animations API by the AnimationNode interface.

[AnimationNodeList](/apis/web_animations/AnimationNodeList)
:   The sole reason this interface exists is to provide a familiar experience for authors familiar with DOM interfaces where child nodes are accessed via a children member.

[AnimationPlayerEvent](/apis/web_animations/AnimationPlayerEvent)
:   Constructs a new AnimationPlayerEvent object as described in Constructing events in [DOM4].

    <http://www.w3.org/TR/dom/#constructing-events>

[AnimationSequence](/apis/web_animations/AnimationSequence)
:   Animation sequences are represented by the AnimationSequence interface.

[AnimationTiming](/apis/web_animations/AnimationTiming)
:   Timing parameters for an AnimationNode are collected together under the AnimationTiming type.

[CompositeOperation](/apis/web_animations/CompositeOperation)
:   The possible values of an animation effect’s composition behavior are represented by the CompositeOperation enumeration.

[ComputedTimingProperties](/apis/web_animations/ComputedTimingProperties)
:

[IterationCompositeOperation](/apis/web_animations/IterationCompositeOperation)
:   The possible values of an animation effect’s iteration composite operation are represented by the IterationCompositeOperation enumeration.

[MotionPathEffect](/apis/web_animations/MotionPathEffect)
:   Motion path animation effects are represented by the MotionPathEffect interface.

## <span>See also</span>

### <span>Related articles</span>

#### <span>Animation</span>

-   **Web Animations API**

-   [clone](/apis/web_animations/AnimationEffect/clone)

-   [AnimationNode](/apis/web_animations/AnimationNode)

-   [timing](/apis/web_animations/AnimationNode/timing)

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

### <span>External resources</span>

W3C Web Animations Specification, Editors Draft <http://w3c.github.io/web-animations/>