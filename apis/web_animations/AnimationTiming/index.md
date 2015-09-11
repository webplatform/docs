---
title: AnimationTiming
readiness: 'Almost Ready'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: AnimationTimingReadOnly
    href: /apis/web_animations/AnimationTimingReadOnly
standardization_status: 'W3C Editor''s Draft'
summary: 'Timing parameters for an AnimationNode are collected together under the AnimationTiming type.'
tags:
  - API
  - Objects
  - Web
  - Animations
uri: 'apis/web animations/AnimationTiming'

---
## <span>Summary</span>

Timing parameters for an AnimationNode are collected together under the AnimationTiming type.

Inherits from [AnimationTimingReadOnly](/apis/web_animations/AnimationTimingReadOnly)[AnimationTimingReadOnly](/apis/web_animations/AnimationTimingReadOnly)

## <span>Properties</span>

*No properties.*

## <span>Methods</span>

*No methods.*

## <span>Events</span>

*No events.*

## <span>Inherited from AnimationTimingReadOnly</span>

### <span>Properties</span>

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

### <span>Methods</span>

*No methods.*

### <span>Events</span>

*No events.*

**Needs Examples**: This section should include examples.

