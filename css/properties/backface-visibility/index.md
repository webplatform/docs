---
title: backface-visibility
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/backface-visibility)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5306741'
  - 'http://gist.github.com/5306757'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`visible`'
  'Applies to': 'transformable elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'Same as specified value.'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`backfaceVisibility`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Determines whether or not the “back” side of a transformed element is visible when facing the viewer.'
tags:
  - CSS
  - Properties
uri: css/properties/backface-visibility

---
## <span>Summary</span>

Determines whether or not the “back” side of a transformed element is visible when facing the viewer.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `visible`

Applies to
:   transformable elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   Same as specified value.

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `backfaceVisibility`

Percentages
:   N/A

## <span>Syntax</span>

-   `backface-visibility: hidden`
-   `backface-visibility: visible`

## <span>Values</span>

visible
:   The back face of an element is a transparent background, displaying a mirror image of the front face when the back face is observable.

hidden
:   There are cases when we do not want the front face of an element to be visible through the back face, like when doing a flipping card effect (setting two elements side-to-side). In this case, the property should be set to hidden to make the back face of the element opaque.

## <span>Examples</span>

``` css
backface-visibility: visible;
```

[View live example](http://code.webplatform.org/gist/5306741)

``` css
backface-visibility: hidden;
```

[View live example](http://code.webplatform.org/gist/5306757)

This property disables position: fixed on Firefox, see related bug: <https://bugzilla.mozilla.org/show_bug.cgi?id=876341>

## <span>Related specifications</span>

[CSS Transforms Level 1](http://www.w3.org/TR/css3-transforms/#backface-visibility-property)
:   W3C Working Draft

## <span>See also</span>

### <span>Related articles</span>

#### <span>Transforms</span>

-   [inverse](/css/cssom/MSCSSMatrix/methods/inverse)

-   [multiply](/css/cssom/MSCSSMatrix/methods/multiply)

-   [rotate](/css/cssom/MSCSSMatrix/methods/rotate)

-   [rotate3d()](/css/functions/rotate3d())

-   [scale3d()](/css/functions/scale3d())

-   [skew()](/css/functions/skew())

-   [translate()](/css/functions/translate())

-   [translate3d()](/css/functions/translate3d())

-   [translateX()](/css/functions/translateX())

-   [translateY()](/css/functions/translateY())

-   [translateZ()](/css/functions/translateZ())

-   **backface-visibility**

-   [transform-origin-z](/css/properties/transform-origin-z)

-   [MSCSSMatrix](/css/transforms/MSCSSMatrix)

-   [translate](/css/transforms/MSCSSMatrix/translate)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)
