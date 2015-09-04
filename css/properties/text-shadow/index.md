---
title: text-shadow
tags:
  0: CSS
  1: Properties
  3: Design
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The CSS text-shadow property applies one or more drop shadows to the text and <text-decorations> of an element. Each shadow is specified as an offset from the text, along with optional color and blur radius values.'
code_samples:
  - 'http://gist.github.com/5842702'
  - 'http://gist.github.com/5864800'
  - 'http://gist.github.com/5864841'
uri: css/properties/text-shadow

---
# text-shadow

## Summary

The CSS text-shadow property applies one or more drop shadows to the text and \<text-decorations\> of an element. Each shadow is specified as an offset from the text, along with optional color and blur radius values.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `none`
Applies to
:   all elements
[Inherited](/css/concepts/inherited)
:   Yes
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   a color plus three absolute lengths
Animatable
:   Yes, as shadow list
[CSS Object Model Property](/css/concepts/cssom)
:   `textShadow`
Percentages
:   N/A

## Syntax

-   `text-shadow: <blur-radius>`
-   `text-shadow: <color>`
-   `text-shadow: <offset-x>`
-   `text-shadow: <offset-y>`
-   `text-shadow: none`

## Values

none
:   Default value.

\<offset-x\>
:   Required. Specifies the horizontal `<length>` term to the right of the text. A negative horizontal `<length>` term will place the shadow to the left of the text.

\<offset-y\>
:   Required. Specifies the vertical `<length>` value below the text. A negative vertical `<length>` term will place the shadow above the text.

\<blur-radius\>
:   Optional. The blur radius is a `<length>` term that indicates the boundaries of the blur effect.

\<color\>
:   Optional. A color value may be applied before or after the `<length>` terms of both shadow effects. The color value will be inherited as the basis for the shadow. If a color is not specified by the user, the value of the color property will be used instead.

## Examples

``` {.css}
*/ This example uses all four values of the text-shadow property in the following order: <offset-x>, <offset-y>, <blur-radius>, and <color>. /*

p {
  text-shadow: 2px 2px 2px grey;
}
```

[View live example](http://code.webplatform.org/gist/5842702)

``` {.css}
*/ This example uses both required offset values, <offset-x> and <offset-y>. The optional <blur-radius> and <color> values have been omitted. /*

p {
  text-shadow: -0.1em -0.1em;
}
```

[View live example](http://code.webplatform.org/gist/5864800)

``` {.css}
*/ This example shows multiple shadow effects separated by a comma. Note the use of various units and color models applied to the values. /*

p {
  text-shadow: -0.1em -0.1em 1em purple, 3px 3px 0.1em rgba(0, 0, 0, 0.5);
}
```

[View live example](http://code.webplatform.org/gist/5864841)

## Usage

     The text-shadow property can also be used to draw outlines, bevels, and other effects.

## Notes

Multiple shadows are applied front-to-back, with the first-specified shadow on top.

The `text-shadow` property applies to both the ::first-line and ::first-letter pseudo-elements.

## Related specifications

Specification
:   Status
[CSS Text Decoration Module Level 3](http://www.w3.org/TR/css-text-decor-3/#text-shadow-property)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/Web/CSS/text-shadow)

