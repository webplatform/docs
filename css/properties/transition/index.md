---
title: transition
tags:
  0: CSS
  1: Properties
  3: Vendor
  4: Prefix
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The transition CSS property is a shorthand property for transition-property, transition-duration, transition-timing-function, and transition-delay. It allows to define the transition between two states of an element.'
code_samples:
  - 'http://gist.github.com/5842511'
uri: css/properties/transition

---
# transition

## Summary

The transition CSS property is a shorthand property for transition-property, transition-duration, transition-timing-function, and transition-delay. It allows to define the transition between two states of an element.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `see individual properties`
Applies to
:   all elements, :before and :after pseudo elements
[Inherited](/css/concepts/inherited)
:   No
Media
:   interactive
[Computed value](/css/concepts/computed_value)
:   as specified
Animatable
:   No
[CSS Object Model Property](/css/concepts/cssom)
:   `transition`
Percentages
:   N/A

## Syntax

-   `transition: transition-delay`
-   `transition: transition-duration`
-   `transition: transition-property`
-   `transition: transition-timing-function`

## Values

transition-property
:   Value of the [**transition-property**](/css/properties/transition-property) property.

transition-duration
:   Value of the [**transition-duration**](/css/properties/animation-duration) property.

transition-timing-function
:   Value of the [**transition-timing-function**](/css/properties/animation-timing-function) property.

transition-delay
:   Value of the [**transition-delay**](/css/properties/animation-delay) property.

## Examples

When you hover over the div, the height property will gradually change from 100 to 500.

``` {.css}
/*
 * This example usage of the transition shorthand
 *
 * In this example the height of a div will change
 * to 300px over 2 seconds.
 *
 * The non-shorthand equivalent would be:
 * transition-property: height;
 * transition-duration: 2s;
 */

div:hover {
  height: 300px;
  transition: height 2s;
}
```

[View live example](http://code.webplatform.org/gist/5842511)

A list of translatable properties exists here: [http://www.w3.org/TR/2009/WD-css3-transitions-20091201/\#animatable-properties-](http://www.w3.org/TR/2009/WD-css3-transitions-20091201/#animatable-properties-)

## Related specifications

Specification
:   Status
[CSS Transitions](http://www.w3.org/TR/2009/WD-css3-transitions-20091201/)
:   W3C Working Draft

## See also

### Related articles

#### Animation

-   [Web Animations API](/apis/web_animations)

-   [clone](/apis/web_animations/AnimationEffect/clone)

-   [AnimationNode](/apis/web_animations/AnimationNode)

-   [timing](/apis/web_animations/AnimationNode/timing)

-   [currentTime](/apis/web_animations/AnimationPlayer/currentTime)

-   [reverse](/apis/web_animations/AnimationPlayer/reverse)

-   [source](/apis/web_animations/AnimationPlayer/source)

-   [AnimationPlayerEvent](/apis/web_animations/AnimationPlayerEvent)

-   [currentTime](/apis/web_animations/AnimationTimeline/currentTime)

-   [play](/apis/web_animations/AnimationTimeline/play)

-   [AnimationTimingReadOnly](/apis/web_animations/AnimationTimingReadOnly)

-   [@keyframes](/css/atrules/@keyframes)

-   [CSSKeyframeRule](/css/cssom/CSSKeyframeRule)

-   [keyText](/css/cssom/CSSKeyframeRule/keyText)

-   [style](/css/cssom/CSSKeyframeRule/style)

-   [CSSKeyframesRule](/css/cssom/CSSKeyframesRule)

-   [cssRules](/css/cssom/CSSKeyframesRule/cssRules)

-   [deleteRule](/css/cssom/CSSKeyframesRule/deleteRule)

-   [findRule](/css/cssom/CSSKeyframesRule/findRule)

-   [insertRule](/css/cssom/CSSKeyframesRule/insertRule)

-   [name](/css/cssom/CSSKeyframesRule/name)

-   [cubic-bezier](/css/functions/cubic-bezier)

-   [Animations](/css/properties/animations)

-   **transition**

-   [SVG animation](/svg/tutorials/smarter_svg_animation)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

#### Transitions

-   [cubic-bezier](/css/functions/cubic-bezier)

-   **transition**

-   [transition-delay](/css/properties/transition-delay)

-   [transition-duration](/css/properties/transition-duration)

-   [transition-property](/css/properties/transition-property)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/transition)

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

