---
title: animation-timing-function
tags:
  - CSS
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Describes how the animation will progress over one cycle of its duration.'
code_samples:
  - 'http://gist.github.com/7011239'
uri: css/properties/animation-timing-function

---
# animation-timing-function

## Summary

Describes how the animation will progress over one cycle of its duration.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `ease`
Applies to
:   all elements, ::before and ::after pseudo-elements
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   As specified.
Animatable
:   No
[CSS Object Model Property](/css/concepts/cssom)
:   `animationTimingFunction`
Percentages
:   N/A

## Syntax

-   `animation-timing-function: cubic-bezier(0,0,1,1)`
-   `animation-timing-function: ease`
-   `animation-timing-function: ease-in`
-   `animation-timing-function: ease-in-out`
-   `animation-timing-function: ease-out`
-   `animation-timing-function: linear`
-   `animation-timing-function: step-end`
-   `animation-timing-function: step-start`
-   `animation-timing-function: steps(3, end)`

## Values

ease
:   Default. The animation begins and ends gradually; this value is equivalent to `cubic-bezier(0.25,0.1,0.25,1)`.

linear
:   The animation begins and progresses at a constant rate over the specified duration; this value is equivalent to `cubic-bezier(0,0,1,1)`

ease-in
:   The animation begins gradually and progresses at a steady rate; this value is equivalent to `cubic-bezier(0.42,0,1,1)`.

ease-out
:   The animation begins at a steady rate then gradually ends; this value is equivalent to `cubic-bezier(0,0,0.58,1)`.

ease-in-out
:   The animation begins and ends gradually; equivalent to `cubic-bezier(0.42,0,0.58,1)`. Note that this timing function is similar to `ease`, although the latter starts faster than it ends.

cubic-bezier(0,0,1,1)
:   Specifies a cubic bezier curve. The four values specify points P1 and P2 of the curve as (x1, y1, x2, y2). Both x values must be in the range [0, 1] or the definition is invalid. The y values can exceed this range. This function is used to specify custom timing functions.

steps(3, end)
:   Specifies a stepping function using two parameters. The first parameter specifies the number of intervals in the function. It must be a positive integer greater than 0. The second optional is either the value `start` or `end` and specifies the point at which the change of values occur within the interval. If the second parameter is omitted, it is given the value `end`.

step-start
:   Equivalent to steps(1,start).

step-end
:   Equivalent to steps(1,end).

## Examples

A fast-moving sequence uses linear timing to highlight an abrupt transition within the keyframes, from a moving to a stopped state:

``` {.css}
div {
    animation-duration        : 0.5s;
    animation-fill-mode       : both;
    animation-iteration-count : 1;
    animation-name            : fastSlide;
    animation-timing-function : linear;
    transform-origin          : bottom;
}
@keyframes fastSlide {
    0%   { transform: translate(120%) skewX(-30deg) ; }
    70%  { transform: translate(0%)   skewX(-30deg) ; }
    80%  { transform: translate(0%)   skewX(20deg)  ; }
    95%  { transform: translate(0%)   skewX(-10deg) ; }
    100% { transform: translate(0%)   skewX(0deg)   ; }
}
```

[View live example](http://code.webplatform.org/gist/7011239)

## Usage

     The timing functions supported by animation-timing-function are defined by transition-timing-function.

If `animation-timing-function` specifies more timing functions than there are values in `animation-name`, the excess functions are ignored. If `animation-timing-function` specifies fewer durations than there are values in `animation-name`, the list of functions is repeated as many times as necessary to ensure each animation has a duration.

For a keyframed animation, the **animation-timing-function** applies between keyframes, not over the entire animation. For example, in the case of an **ease-in-out** timing function, an animation will ease in at the start of the keyframe and ease out at the end of the keyframe. An **animation-timing-function** defined within a keyframe block applies to that keyframe, otherwise the timing function specified for the animation is used.

## Related specifications

Specification
:   Status
[CSS Animations](http://www.w3.org/TR/css3-animations/)
:   Working Draft

## See also

### Other articles

-   [Making things move with CSS3 animations](/tutorials/css_animations)
-   [@keyframes](/css/atrules/@keyframes)
-   [animation](/css/properties/animation)
-   [animation-delay](/css/properties/animation-delay)
-   [animation-direction](/css/properties/animation-direction)
-   [animation-duration](/css/properties/animation-duration)
-   [animation-fill-mode](/css/properties/animation-fill-mode)
-   [animation-iteration-count](/css/properties/animation-iteration-count)
-   [animation-name](/css/properties/animation-name)
-   [animation-play-state](/css/properties/animation-play-state)

### External resources

-   A [detailed description of timing functions](https://developer.mozilla.org/en-US/docs/Web/CSS/timing-function) (MDN)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/).

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

