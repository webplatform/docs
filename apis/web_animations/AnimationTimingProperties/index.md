---
title: 'AnimationTimingProperties'
readiness: 'Almost Ready'
standardization_status: 'W3C Editor''s Draft'
summary: 'The AnimationTimingProperties dictionary is encapsulates the timing properties of an AnimationNode so that they can be set in bulk (as in the constructor for Animation) or returned as a readonly snapshot (as in computedTiming).'
tags:
  - API_Objects
  - Web_Animations
  - Needs_Examples
uri: 'apis/web animations/AnimationTimingProperties'

---
## Summary

The AnimationTimingProperties dictionary is encapsulates the timing properties of an AnimationNode so that they can be set in bulk (as in the constructor for Animation) or returned as a readonly snapshot (as in computedTiming).

## Properties

[delay](/apis/web_animations/AnimationTimingProperties/delay)
:   The specified start delay.

    See the description of the delay attribute on the AnimationTiming interface.

[direction](/apis/web_animations/AnimationTimingProperties/direction)
:   See the direction member of the AnimationTimingReadOnly interface.

[duration](/apis/web_animations/AnimationTimingProperties/duration)
:   See the duration member of the AnimationTimingReadOnly interface.

    Real numbers less than zero, NaN values, and strings other than the lowercase value auto are treated the same as auto for the purpose of timing model calculations.

[easing](/apis/web_animations/AnimationTimingProperties/easing)
:   See the easing member of the AnimationTimingReadOnly interface.

    Unrecognized string values or values that correspond to a timing function that is not supported for the type of animation node to which this property is applied are treated as if the linear keyword was specified for the purpose of timing model calculations.

[endDelay](/apis/web_animations/AnimationTimingProperties/endDelay)
:   The specified end delay.

    See the description of the endDelay attribute on the AnimationTiming interface.

[fill](/apis/web_animations/AnimationTimingProperties/fill)
:   See the fill member of the AnimationTimingReadOnly interface.

[interations](/apis/web_animations/AnimationTimingProperties/interations)
:   See the iterations member of the AnimationTimingReadOnly interface.

    Values less than zero and NaN values are treated as the value 1.0 for the purpose of timing model calculations.

[iterationStart](/apis/web_animations/AnimationTimingProperties/iterationStart)
:   See the iterationStart member of the AnimationTimingReadOnly interface.

    Values less than zero are clamped to zero for the purpose of timing model calculations.

    Note that the value of iterations is effectively added to the iterationStart such that an animation node with an iterationStart of ‘0.5’ and iterations of ‘2’ would still repeat twice however it would begin and end half-way through the animation node’s iteration interval. Setting the iterationStart to a value greater than or equal to one is typically only useful in combination with an animation effect that has an iteration composite operation of ‘accumulate’.

[playbackRate](/apis/web_animations/AnimationTimingProperties/playbackRate)
:   See the playbackRate member of the AnimationTimingReadOnly interface.

## Methods

*No methods.*

## Events

*No events.*
