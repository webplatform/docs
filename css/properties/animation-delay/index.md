---
title: 'animation-delay'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/animation-delay)'
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
code_samples:
  - 'http://code.webplatform.org/gist/7011569'
  - 'http://code.webplatform.org/gist/7012307'
compatibility:
  feature: animation-delay
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`0s`'
  'Applies to': 'All elements, ::before and ::after pseudo-elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified.'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`animationDelay`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Defines a length of time to elapse before an animation starts, allowing an animation to begin execution some time after it is applied.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/animation-delay

---
## Summary

Defines a length of time to elapse before an animation starts, allowing an animation to begin execution some time after it is applied.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `0s`

Applies to
:   All elements, ::before and ::after pseudo-elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified.

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `animationDelay`

Percentages
:   N/A

## Syntax

-   `animation-delay: <time>`

## Values

\<time\>
:   Can be specified in seconds or milliseconds, e.g., **2s** or **150ms**. Can also be a comma-separated list of delays, e.g., **.25s, .5s, 1s**, where each delay is applied to the corresponding ordinal position value of the [animation-name](/css/properties/animation-name) property.

*If the value is negative the animation will execute the moment it is applied, but will begin execution at the specified offset. That is, the animation appears to begin part-way through its cycle.*

## Examples

A delay of 5 seconds.

``` css
div.animationDelay {
    animation-delay: 5s;
}
```

[View live example](http://code.webplatform.org/gist/7011569)

An example of a mobile-like interface in which concurrent *moveContent* and *insertBanner* animations introduce a colored banner header after a 4-second delay. A subsequent *scrollBanner* animation uses a similar delay to start 5 seconds after the page loads.

``` css
article {
    animation-name : moveContent;
    animation-duration : 1s;
    animation-delay : 4s;
    animation-iteration-count : 1;
    animation-fill-mode : forwards;
}

header {
    animation-name : insertBanner , scrollBanner;
    animation-duration : 1s , 20s;
    animation-delay : 4s , 5s;
    animation-fill-mode : backwards , none;
    animation-iteration-count : 1 , infinite;
}


@keyframes moveContent {
    from { transform : translateY(0em) }
    to   { transform : translateY(3em) }
}

@keyframes insertBanner {
    from { transform : translateY(-6em) }
    to   { transform : translateY(0em) }
}

@keyframes scrollBanner {
    from { transform : translateX(0) }
    17%  { transform : translateX(0%) }
    20%  { transform : translateX(-20%) }
    37%  { transform : translateX(-20%) }
    40%  { transform : translateX(-40%) }
    57%  { transform : translateX(-40%) }
    60%  { transform : translateX(-60%) }
    77%  { transform : translateX(-60%) }
    80%  { transform : translateX(-80%) }
    97%  { transform : translateX(-80%) }
    to   { transform : translateX(0%) }
}
```

[View live example](http://code.webplatform.org/gist/7012307)

## Usage

     *If animation-delay specifies more delays than there are values in animation-name, the excess delays are ignored.

-   If `animation-delay` specifies fewer delays than there are values in `animation-name`, the list of delays is repeated as many times as needed to map each animation to a delay.

## Related specifications

[CSS Animations](http://www.w3.org/TR/css3-animations/#animation-delay-property)
:   Working Draft

## See also

### Other articles

-   [Making things move with CSS3 animations](/tutorials/css_animations)
-   [@keyframes](/css/atrules/@keyframes)
-   [animation](/css/properties/animation)
-   [animation-direction](/css/properties/animation-direction)
-   [animation-duration](/css/properties/animation-duration)
-   [animation-fill-mode](/css/properties/animation-fill-mode)
-   [animation-iteration-count](/css/properties/animation-iteration-count)
-   [animation-name](/css/properties/animation-name)
-   [animation-play-state](/css/properties/animation-play-state)
-   [animation-timing-function](/css/properties/animation-timing-function)
