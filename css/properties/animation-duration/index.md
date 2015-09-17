---
title: 'animation-duration'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
code_samples:
  - 'http://gist.github.com/7010824'
  - 'http://gist.github.com/7010365'
compatibility:
  feature: animation-duration
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`0s`'
  'Applies to': 'All elements, ::before and ::after pseudo-elements.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified.'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`animationDuration`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Defines the length of time an animation takes to complete one cycle.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/animation-duration

---
## Summary

Defines the length of time an animation takes to complete one cycle.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `0s`

Applies to
:   All elements, ::before and ::after pseudo-elements.

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified.

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `animationDuration`

Percentages
:   N/A

## Syntax

-   `animation-duration: <time>`

## Values

\<time\>
:   Can be specified in seconds or milliseconds, e.g., **2s** or **150ms**. Can also be a comma-separated list of durations, e.g., **.25s, .5s, 1s**, where each duration is applied to the corresponding ordinal position value of the [animation-name](/css/properties/animation-name) property.

The initial value of 0s means the animation takes no time; that is, it is applied instantaneously. When the duration is 0s (or 0ms), [animation-fill-mode](/css/properties/animation-fill-mode) still applies, such that an animation filling backward will show the value of the 0% [keyframe](/css/atrules/@keyframes) during any [delay](/css/properties/animation-delay) period, while an animation filling forward will retain the value specified at the 100% [keyframe](/css/atrules/@keyframes) even if the animation was instantaneous. Also, animation events are still fired.

## Examples

An animation duration of 5 seconds; runs once, does not repeat.

``` css
div.duration {
    animation-duration: 5s;
}
```

[View live example](http://gist.github.com/7010824)

A repeating pulse animation that shrinks and dims an element, then restores it.

``` css
div.selected {
    animation-name: pulse;
    animation-duration: 1s;
    animation-iteration-count: infinite;
}

@keyframes pulse {
    from {
        transform : scale(1) translateX(0);
        opacity : 1;
    }
    50% {
        transform : scale(0.75) translateX(0);
        opacity : 0.25;
    }
    to {
        transform : scale(1) translateX(0);
        opacity : 1;
    }
}
```

[View live example](http://gist.github.com/7010365)

## Usage

     *Negative duration values are invalid and cause the entire property value to be ignored.

-   If `animation-duration` specifies more durations than there are values in `animation-name`, the excess durations are ignored.
-   If `animation-duration` specifies fewer durations than there are values in `animation-name`, the list of durations is repeated as many times as necessary to ensure each animation has a duration.

## Related specifications

[CSS Animations](http://www.w3.org/TR/css3-animations/)
:   Working Draft

## See also

### Other articles

-   [Making things move with CSS3 animations](/tutorials/css_animations)
-   [@keyframes](/css/atrules/@keyframes)
-   [animation](/css/properties/animation)
-   [animation-delay](/css/properties/animation-delay)
-   [animation-direction](/css/properties/animation-direction)
-   [animation-fill-mode](/css/properties/animation-fill-mode)
-   [animation-iteration-count](/css/properties/animation-iteration-count)
-   [animation-name](/css/properties/animation-name)
-   [animation-play-state](/css/properties/animation-play-state)
-   [animation-timing-function](/css/properties/animation-timing-function)
