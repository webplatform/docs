---
title: AnimationTimingReadOnly
tags:
  0: API
  1: Objects
  3: Web
  4: Animations
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
summary: 'Readonly class from which AnimationTiming classes are inherited. '
uri: 'apis/web animations/AnimationTimingReadOnly'

---
# AnimationTimingReadOnly

## Summary

Readonly class from which AnimationTiming classes are inherited.

## Properties

API Name
:   Summary
[delay](/apis/web_animations/AnimationTimingReadOnly/delay)
:   The start delay which represents the number of milliseconds from an animation node’s start time to the start of the active interval.
[direction](/apis/web_animations/AnimationTimingReadOnly/direction)
:   The playback direction of the animation node as specified by one of the PlaybackDirection enumeration values.
[duration](/apis/web_animations/AnimationTimingReadOnly/duration)
:   The iteration duration which is a real number greater than or equal to zero (including positive infinity) representing the time taken to complete a single iteration of the animation node.
[easing](/apis/web_animations/AnimationTimingReadOnly/easing)
:   The timing function used to scale the time to produce easing effects.
[endDelay](/apis/web_animations/AnimationTimingReadOnly/endDelay)
:   The end delay which represents the number of milliseconds from the end of an animation node’s active interval until the start time of any animation node that may follow, for example, in an animation sequence.
[fill](/apis/web_animations/AnimationTimingReadOnly/fill)
:   The fill mode as specified by one of the FillMode enumeration values.

    When performing timing calculations the special value auto is expanded to one of the fill modes recognized by the timing model as follows,

    If the animation node to which the fill mode is being is applied is an animation, Use none as the fill mode. Otherwise, Use both as the fill mode.

[iterationStart](/apis/web_animations/AnimationTimingReadOnly/iterationStart)
:   The animation node’s iteration start property.

    A finite real number greater than or equal to zero representing the number of iterations into the animation node at which to begin.

[iterations](/apis/web_animations/AnimationTimingReadOnly/iterations)
:   The animation node’s iteration count property.

    A real number greater than or equal to zero (including positive infinity) representing the number of times to repeat the animation node.

[playbackRate](/apis/web_animations/AnimationTimingReadOnly/playbackRate)
:   The animation node’s playback rate property.

## Methods

*No methods.*

## Events

*No events.*

**Needs Examples**: This section should include examples.

## See also

### Related articles

#### Animation

-   [Web Animations API](/apis/web_animations)

-   [clone](/apis/web_animations/AnimationEffect/clone)

-   [AnimationNode](/apis/web_animations/AnimationNode)

-   [timing](/apis/web_animations/AnimationNode/timing)

-   [currentTime](/apis/web_animations/AnimationPlayer/currentTime)

-   [reverse](/apis/web_animations/AnimationPlayer/reverse)

-   [source](/apis/web_animations/AnimationPlayer/source)

-   [AnimationPlayerEvent](/apis/web_animations/AnimationPlayerEvent)

-   [currentTime](/apis/web_animations/AnimationTimeline/currentTime)

-   [play](/apis/web_animations/AnimationTimeline/play)

-   **AnimationTimingReadOnly**

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

