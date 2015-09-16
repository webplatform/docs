---
title: animation-fill-mode
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/Web/CSS/animation-fill-mode)'
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
code_samples:
  - 'http://gist.github.com/7012307'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'All elements, ::before and ::after pseudo-elements.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified.'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: "Defines what values are applied by the animation outside the time it is executing (before and after the animation). \n"
tags:
  - CSS
  - Properties
uri: css/properties/animation-fill-mode

---
## Summary

Defines what values are applied by the animation outside the time it is executing (before and after the animation).

By default, an animation does not affect property values between the time it is applied (when the [animation-name](/css/properties/animation-name) property is set on an element) and the time it begins execution (determined by the [animation-delay](/css/properties/animation-delay) property). Also, by default an animation does not affect property values after the animation ends (determined by the [animation-duration](/css/properties/animation-duration) property). The **animation-fill-mode** property can override this behavior.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `none`

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

-   `animation-fill-mode: backwards`
-   `animation-fill-mode: both`
-   `animation-fill-mode: forwards`
-   `animation-fill-mode: none`

## Values

none
:   Property values do not change before the animation starts, and they return to their original state when the animation ends. This is the default behavior.

forwards
:   When the animation ends (as determined by its [animation-iteration-count](/css/properties/animation-iteration-count)), properties retain the values set by the final keyframe. If **animation-iteration-count** is zero, apply the values that would start the first iteration.

<dl>
<dd>
|[animation-direction](/css/properties/animation-direction)|[animation-iteration-count](/css/properties/animation-iteration-count)|last keyframe encountered|
|:---------------------------------------------------------|:---------------------------------------------------------------------|:------------------------|
|`normal`|`even` or `odd`|100% or `to`|
|`reverse`|`even` or `odd`|0% or `from`|
|`alternate`|`even`|0% or `from`|
|`alternate`|`odd`|100% or `to`|
|`alternate-reverse`|`even`|100% or `to`|
|`alternate-reverse`|`odd`|0% or `from`|

</dd>
</dl>

backwards
:   If the animation is delayed by [animation-delay](/css/properties/animation-delay), properties assume values set by the first keyframe while waiting for the animation to start. These are either the values of the *from* keyframe (when [animation-direction](/css/properties/animation-direction) is **normal** or **alternate**) or those of the *to* keyframe (when [animation-direction](/css/properties/animation-direction) is **reverse** or **alternate-reverse**). When the animation ends, properties revert to their original state.

<dl>
<dd>
|[animation-direction](/css/properties/animation-direction)|first relevant keyframe|
|:---------------------------------------------------------|:----------------------|
|`normal` or `alternate`|0% or `from`|
|`reverse` or `alternate-reverse`|100% or `to`|

</dd>
</dl>

both
:   Values set by the first and last keyframes are applied before and after the animation.

## Examples

An example of a mobile-like interface in which two concurrent animations displace content with a banner header. Without any animations, both elements would overlay the same screen area. In the *moveContent* animation, the fill mode of **forwards** means its end state (moved downward) persists after it finishes executing. In the *insertBanner* animation, the fill mode of **backwards** means its start state (off-screen) takes precedence over the element's CSS during the delay before the animation executes. (In the subsequent *scrollBanner* animation, the fill-mode is explicitly set to **none** to keep its initial state from overriding that of the previous animation.)

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

     Can also be a comma-separated list of fill modes, e.g., forwards, none, backwards, where each fill mode is applied to the corresponding ordinal position value of the animation-name property.

## Notes

This is an experimental specification, and therefore not completely finalized. Syntax and behavior are still subject to change in future versions.

## Related specifications

[CSS Animation](http://www.w3.org/TR/css3-animations/)
:   W3C Working Draft

## See also

### Other articles

-   [Making things move with CSS3 animations](/tutorials/css_animations)
-   [@keyframes](/css/atrules/@keyframes)
-   [animation](/css/properties/animation)
-   [animation-delay](/css/properties/animation-delay)
-   [animation-direction](/css/properties/animation-direction)
-   [animation-duration](/css/properties/animation-duration)
-   [animation-iteration-count](/css/properties/animation-iteration-count)
-   [animation-name](/css/properties/animation-name)
-   [animation-play-state](/css/properties/animation-play-state)
-   [animation-timing-function](/css/properties/animation-timing-function)

### External resources

-   See also [Val Head's examples with tutorial video](http://www.valhead.com/2013/01/04/tutorial-css-animation-fill-mode/).
