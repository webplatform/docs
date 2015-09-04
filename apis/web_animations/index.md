---
title: web animations
tags:
  0: API
  1: Listings
  3: Web
  4: Animations
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
notes:
  - 'API documentation needs to be competed.'
summary: 'Javascript programming interface for modeling synchronizing and timing the changes to a web page''s presentation.'
uri: 'apis/web animations'

---
# Web Animations API

## Summary

Javascript programming interface for modeling synchronizing and timing the changes to a web page's presentation.

API Name
:   Summary
[Animatable](/apis/web_animations/Animatable)
:   Objects that may be the target of an [**Animation**](/apis/web_animations/Animation) implement the Animatable interface.
[Animation](/apis/web_animations/Animation)
:   Animations are represented by the Animation interface.
[AnimationEffect](/apis/web_animations/AnimationEffect)
:   Animation effects are represented by the AnimationEffect interface. AnimationEffect is an abstract interface of which several concrete subinterfaces are provided.
[AnimationGroup](/apis/web_animations/AnimationGroup)
:   Animation groups are represented by the AnimationGroup interface.
[AnimationNode](/apis/web_animations/AnimationNode)
:   Animation nodes are represented in the Web Animations API by the AnimationNode interface.
[AnimationNodeList](/apis/web_animations/AnimationNodeList)
:   The sole reason this interface exists is to provide a familiar experience for authors familiar with DOM interfaces where child nodes are accessed via a children member.
[AnimationPlayer](/apis/web_animations/AnimationPlayer)
:   Represents a single animation player. Players connect animation node, or source, to a timeline and provides playback controls.
[AnimationPlayerEvent](/apis/web_animations/AnimationPlayerEvent)
:   Constructs a new AnimationPlayerEvent object as described in Constructing events in [DOM4].

    [http://www.w3.org/TR/dom/\#constructing-events](http://www.w3.org/TR/dom/#constructing-events)

[AnimationSequence](/apis/web_animations/AnimationSequence)
:   Animation sequences are represented by the AnimationSequence interface.
[AnimationTimeline](/apis/web_animations/AnimationTimeline)
:   Representation of a timeline, including the document timeline.
[AnimationTiming](/apis/web_animations/AnimationTiming)
:   Timing parameters for an AnimationNode are collected together under the AnimationTiming type.
[AnimationTimingProperties](/apis/web_animations/AnimationTimingProperties)
:   The AnimationTimingProperties dictionary is encapsulates the timing properties of an AnimationNode so that they can be set in bulk (as in the constructor for Animation) or returned as a readonly snapshot (as in computedTiming).
[AnimationTimingReadOnly](/apis/web_animations/AnimationTimingReadOnly)
:   Readonly class from which AnimationTiming classes are inherited.
[CompositeOperation](/apis/web_animations/CompositeOperation)
:   The possible values of an animation effect’s composition behavior are represented by the CompositeOperation enumeration.
[ComputedTimingProperties](/apis/web_animations/ComputedTimingProperties)
:
[IterationCompositeOperation](/apis/web_animations/IterationCompositeOperation)
:   The possible values of an animation effect’s iteration composite operation are represented by the IterationCompositeOperation enumeration.
[KeyframeEffect](/apis/web_animations/KeyframeEffect)
:   Keyframe animation effects are represented by the KeyframeEffect interface.
[MotionPathEffect](/apis/web_animations/MotionPathEffect)
:   Motion path animation effects are represented by the MotionPathEffect interface.

## See also

### Related articles

#### Animation

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

-   [AnimationTimingReadOnly](/apis/web_animations/AnimationTimingReadOnly)

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

-   [SVG animation](/svg/tutorials/smarter_svg_animation)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### External resources

W3C Web Animations Specification, Editors Draft [http://w3c.github.io/web-animations/](http://w3c.github.io/web-animations/)

