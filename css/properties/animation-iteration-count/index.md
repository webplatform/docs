---
title: 'animation-iteration-count'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
code_samples:
  - 'http://gist.github.com/7010365'
compatibility:
  feature: animation-iteration-count
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`1`'
  'Applies to': 'All elements, ::before and ::after pseudo-elements.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified.'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Specifies how many times an animation cycle should play.'
tags:
  - CSS
  - Properties
uri: css/properties/animation-iteration-count

---
## Summary

Specifies how many times an animation cycle should play.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `1`

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
:

Percentages
:   N/A

## Syntax

-   `animation-iteration-count: <single-animation-iteration-count>`
-   `animation-iteration-count: infinite`

## Values

\<single-animation-iteration-count\>
:   The animation plays the specified number of times. Can also be a comma-separated list of counts, e.g., **5, 2, 10**, where each duration is applied to the corresponding ordinal position value of the [animation-name](/css/properties/animation-name) property. Negative values are not allowed. You may specify non-integer values to play part of an animation cycle (for example 0.5 will play half of the animation cycle).

infinite
:   Loop the animation indefinitely.

## Examples

A repeating pulse animation that shrinks and dims an element, then restores it. Change the **animation-iteration-count** from *infinite* to a number to see the effect.

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

[View live example](http://code.webplatform.org/gist/7010365)

## Usage

     This property accepts non-integer values, such as 1.5 or 2.75. If a non-integer value is specified, the animation terminates mid-cycle. Negative numbers are not valid.

This property is often used in conjunction an [animation-direction](/css/properties/animation-direction) value of **alternate**, which will cause the animation to play in reverse on alternate cycles.

## Related specifications

[CSS Animations](http://www.w3.org/TR/css3-animations/)
:   W3C Working Draft

## See also

### Other articles

-   [Making things move with CSS3 animations](/tutorials/css_animations)
-   [@keyframes](/css/atrules/@keyframes)
-   [animation](/css/properties/animation)
-   [animation-delay](/css/properties/animation-delay)
-   [animation-direction](/css/properties/animation-direction)
-   [animation-duration](/css/properties/animation-duration)
-   [animation-fill-mode](/css/properties/animation-fill-mode)
-   [animation-name](/css/properties/animation-name)
-   [animation-play-state](/css/properties/animation-play-state)
-   [animation-timing-function](/css/properties/animation-timing-function)

### External resources

-   [Robert Nyman's examples](http://robertnyman.com/2010/05/06/css3-animations)
