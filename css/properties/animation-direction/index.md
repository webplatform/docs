---
title: 'animation-direction'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
code_samples:
  - 'http://code.webplatform.org/gist/7010365'
compatibility:
  feature: animation-direction
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`normal`'
  'Applies to': 'All elements, ::before and ::after pseudo-elements.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified.'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Defines whether an animation should run in reverse on some or all cycles.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/animation-direction

---
## Summary

Defines whether an animation should run in reverse on some or all cycles.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `normal`

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

-   `animation-direction: alternate`
-   `animation-direction: alternate-reverse`
-   `animation-direction: normal`
-   `animation-direction: reverse`

## Values

normal
:   All iterations of the animation are played as specified.

reverse
:   All iterations of the animation are played in the reverse direction from the way they were specified. When an animation is played in reverse the timing functions are also reversed. For example, when played in reverse an ease-in animation would appear to be an ease-out animation.

alternate
:   The animation cycle iterations that are odd counts are played in the normal direction, and the animation cycle iterations that are even counts are played in a reverse direction, thus reversing direction each cycle. The count to determine if an iteration is even or odd starts at one (odd).

alternate-reverse
:   The animation cycle iterations that are odd counts are played in the reverse direction, and the animation cycle iterations that are even counts are played in a normal direction, again reversing direction each cycle. The count to determine if an iteration is even or odd starts at one (odd).

## Examples

A repeating pulse animation that shrinks and dims an element, then restores it. Change the **animation-direction** from *normal* to a different keyword value to see the effect.

``` css
div.selected {
    animation-name: pulse;
    animation-duration: 0.5s;
    animation-direction: alternate;
    animation-iteration-count: infinite;
}

@keyframes pulse {
    from {
        transform : scale(1) translateX(0);
        opacity : 1;
    }
    to {
        transform : scale(0.75) translateX(0);
        opacity : 0.25;
    }
}
```

[View live example](http://code.webplatform.org/gist/7010365)

## Usage

     Can also be a comma-separated list of directions, e.g., reverse, normal, alternate, where each direction is applied to the corresponding ordinal position value of the animation-name property.

## Related specifications

[CSS Animations](http://www.w3.org/TR/css3-animations/)
:   W3C Working Draft

## See also

### Other articles

-   [Making things move with CSS3 animations](/tutorials/css_animations)
-   [@keyframes](/css/atrules/@keyframes)
-   [animation](/css/properties/animation)
-   [animation-delay](/css/properties/animation-delay)
-   [animation-duration](/css/properties/animation-duration)
-   [animation-fill-mode](/css/properties/animation-fill-mode)
-   [animation-iteration-count](/css/properties/animation-iteration-count)
-   [animation-name](/css/properties/animation-name)
-   [animation-play-state](/css/properties/animation-play-state)
-   [animation-timing-function](/css/properties/animation-timing-function)
