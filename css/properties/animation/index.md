---
title: 'animation'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
code_samples:
  - 'http://gist.github.com/7044978'
compatibility:
  feature: animation
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`See individual properties.`'
  'Applies to': 'All elements, ::before and ::after pseudo-elements.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'See individual properties.'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: 'See individual properties.'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Shorthand property to define a CSS animation, setting all parameters at once.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/animation

---
## Summary

Shorthand property to define a CSS animation, setting all parameters at once.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `See individual properties.`

Applies to
:   All elements, ::before and ::after pseudo-elements.

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   See individual properties.

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   See individual properties.

## Syntax

-   `animation: single-animation [, single-animation]*`

## Values

single-animation [, single-animation]\*
:   A list of values for each of the individual animation properties. The animation name and duration are required; all other values are optional. Multiple animations can be assigned as a comma-separated list.

`<single-animation-name>`
:   Value of the [**animation-name**](/css/properties/animation-name) property.
`<single-animation-duration>`
:   Value of the [**animation-duration**](/css/properties/animation-duration) property.
`<single-animation-timing-function>`
:   Value of the [**animation-timing-function**](/css/properties/animation-timing-function) property.
`<single-animation-delay>`
:   Value of the [**animation-delay**](/css/properties/animation-delay) property.
`<single-animation-iteration-count>`
:   Value of the [**animation-iteration-count**](/css/properties/animation-iteration-count) property.
`<single-animation-direction>`
:   Value of the [**animation-direction**](/css/properties/animation-direction) property.
`<single-animation-fill-mode>`
:   Value of the [**animation-fill-mode**](/css/properties/animation-fill-mode) property.

**Note:** The first `<time>` value is assigned to the **animation-duration**. The second `<time>` value is assigned to the **animation-delay**.

## Examples

See [animation-play-state](/css/properties/animation-play-state) for an example that uses the animation shorthand property.

``` css
nav.expanded > div.selected {
    animation: pulse 1s infinite;
}
```

[View live example](http://gist.github.com/7044978)

## Usage

     The animation shorthand property combines all animation properties except animation-play-state in a single declaration. The name and duration of the animation are required, but all other values are optional. When two <time> values are supplied, the first is assigned to the duration, and the second to the delay.

Values for a single animation are separated by spaces. Multiple animations can be assigned as a comma-separated list.

## Notes

Before the advent of CSS3, most animations were performed by using Javascript to move HTML DOM elements. This was not optimal, as the browser would not know anything about the DOM element it was moving until it executed the Javascript which moved it, making hardware accelerating animations difficult for vendors. So, CSS3's animation module was born.

This module allows browser vendors to better support animations with hardware acceleration, especially important on CPU constrained devices such as mobile devices. Because the browser controls the inbetween state, or *tween* as it is more commonly known, between two animation states, it can fully hardware accelerate the resultant animation. This leads to lower CPU usage, smoother graphics and less battery intensive web pages on mobile devices.

Animations use keyframes to specify points of animation and timing to state when those keyframes should appear. Those keyframes exist in a separate [**@keyframes**](/css/atrules/@keyframes) section in the CSS. The browser automatically handles the "tween" between each keyframe property. Animation is a shorthand property that defines all the properties of an animation in a single declaration. Animation applies to all elements. See the keyframes section linked above for a list of properties that can be animated.

Also, see [this CSS animations tutorial](/tutorials/css_animations).

## Related specifications

[CSS Animations](http://www.w3.org/TR/css3-animations/)
:   W3C Working Draft

## See also

### Other articles

-   [Making things move with CSS3 animations](/tutorials/css_animations)
-   [@keyframes](/css/atrules/@keyframes)
-   [animation-delay](/css/properties/animation-delay)
-   [animation-direction](/css/properties/animation-direction)
-   [animation-duration](/css/properties/animation-duration)
-   [animation-fill-mode](/css/properties/animation-fill-mode)
-   [animation-iteration-count](/css/properties/animation-iteration-count)
-   [animation-name](/css/properties/animation-name)
-   [animation-play-state](/css/properties/animation-play-state)
-   [animation-timing-function](/css/properties/animation-timing-function)
