---
title: animation-name
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
code_samples:
  - 'http://gist.github.com/7009934'
  - 'http://gist.github.com/7010365'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'All elements, ::before and ::after pseudo-elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified.'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`animationName`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Defines the list of animations that apply to the element.'
tags:
  - CSS
  - Properties
uri: css/properties/animation-name

---
## <span>Summary</span>

Defines the list of animations that apply to the element.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `none`

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
:   `animationName`

Percentages
:   N/A

## <span>Syntax</span>

-   `animation-name: <single-animation-name> [, <single-animation-name>]*`
-   `animation-name: none`

## <span>Values</span>

none
:   No animation applies to the element. You can use this value to override any animations coming from the cascade.

\<single-animation-name\> [, \<single-animation-name\>]\*
:   One or more comma-separated animation names. Each name is used to select the `@keyframes` rule that defines the animation. If the specified name does not match any **@keyframes** rule then no animation will be run for this name. In addition, when multiple animations update the same property, the animation listed last wins.

## <span>Examples</span>

A slide-in animation that executes once, much like a transition.

``` css
h1 {
  animation-duration: 3s;
  animation-name: slidein;
}

@keyframes slidein {
  from {
    margin-left: 100%;
    width: 300%
  }

  to {
    margin-left: 0%;
    width: 100%;
  }
}
```

[View live example](http://code.webplatform.org/gist/7009934)

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

[View live example](http://code.webplatform.org/gist/7010365)

## <span>Usage</span>

     Note that animation-name is not sufficient to run an animation. The animation-duration property also needs to be set to a non-zero duration.

When `animation-name` specifies a list of names, other animation properties such as `animation-duration` should define values corresponding to each name. If the lists of values for the other animation properties do not have the same number of values as `animation-name`, the length of the `animation-name` list determines the number of items in each list examined when starting animations. The lists are matched up from the first value: excess values at the end are not used. If one of the other properties doesn't have enough comma-separated values to match the number of values of `animation-name`, the list is repeated until there are enough. This truncation or repetition does not affect the computed value.

## <span>Related specifications</span>

[CSS Animations](http://www.w3.org/TR/css3-animations/)
:   Working Draft

## <span>See also</span>

### <span>Other articles</span>

-   [Making things move with CSS3 animations](/tutorials/css_animations)
-   [@keyframes](/css/atrules/@keyframes)
-   [animation](/css/properties/animation)
-   [animation-delay](/css/properties/animation-delay)
-   [animation-direction](/css/properties/animation-direction)
-   [animation-duration](/css/properties/animation-duration)
-   [animation-fill-mode](/css/properties/animation-fill-mode)
-   [animation-iteration-count](/css/properties/animation-iteration-count)
-   [animation-play-state](/css/properties/animation-play-state)
-   [animation-timing-function](/css/properties/animation-timing-function)
