---
title: 'border-top-left-radius'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Border-top-left-radius](https://developer.mozilla.org/es/docs/CSS/border-top-left-radius) Article]'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/6949445'
compatibility:
  feature: border-top-left-radius
  topic: css
notes:
  - 'Complete summery, example.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`0`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'two absolute \<length\> or percentages'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`borderTopLeftRadius`'
  Percentages: 'Refer to the corresponding dimension of the border box'
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Sets the rounding of the top-left corner of the element.'
tags:
  - CSS
  - Properties
uri: css/properties/border-top-left-radius

---
## Summary

Sets the rounding of the top-left corner of the element.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `0`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   two absolute \<length\> or percentages

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `borderTopLeftRadius`

Percentages
:   Refer to the corresponding dimension of the border box

## Syntax

-   `border-top-left-radius: length`
-   `border-top-left-radius: percentage`

## Values

length
:   Denotes the size of the circle radius or the semi-major and semi-minor axes of the ellipsis. It can be expressed in any unit allowed by the [CSS \<length\> data types](/css/data_types/length). Negative values are invalid.

percentage
:   Denotes the size of the circle radius, or the semi-major and semi-minor axes of the ellipsis, using percentage values. Percentages for the horizontal axis refer to the width of the box, percentages for the vertical axis refer to the height of the box. Negative values are invalid.

## Examples

``` html

```

[View live example](http://code.webplatform.org/gist/6949445)

## Notes

### Remarks

-   The **border-top-left-radius** property specifies the horizontal and vertical radii of the ellipse that defines the rounded upper-left corner for a border box. If there is only one value given, that value specifies both horizontal and vertical radii of the ellipse. If there are two values given, the first value sets the horizontal radius and the second value sets the vertical radius.
-   When animating this property (as a length, percentage or calc()): when both values are lengths, they are interpolated as lengths; when both values are percentages, they are interpolated as percentages; otherwise, both values are converted into a calc() function that is the sum of a length and a percentage (each possibly zero), and these calc() functions have each half interpolated as real numbers.

## Related specifications

[CSS Backgrounds and Borders Module Level 3; 5.1. Curve Radii: the ‘border-radius’ properties](http://www.w3.org/TR/css3-background/#border-top-left-radius)
:   Candidate Recommendation

[CSS Backgrounds and Borders Module Level 3; 5.1. Curve Radii: the ‘border-radius’ properties](http://dev.w3.org/csswg/css-backgrounds/#border-top-left-radius)
:   Editor's Draft

## See also

### Related articles

#### Border

-   [border](/css/properties/border)

-   [border-bottom](/css/properties/border-bottom)

-   [border-bottom-color](/css/properties/border-bottom-color)

-   [border-bottom-left-radius](/css/properties/border-bottom-left-radius)

-   [border-bottom-style](/css/properties/border-bottom-style)

-   [border-bottom-width](/css/properties/border-bottom-width)

-   [border-color](/css/properties/border-color)

-   [border-image](/css/properties/border-image)

-   [border-image-outset](/css/properties/border-image-outset)

-   [border-image-repeat](/css/properties/border-image-repeat)

-   [border-image-slice](/css/properties/border-image-slice)

-   [border-image-source](/css/properties/border-image-source)

-   [border-image-width](/css/properties/border-image-width)

-   [border-left](/css/properties/border-left)

-   [border-left-color](/css/properties/border-left-color)

-   [border-left-style](/css/properties/border-left-style)

-   [border-left-width](/css/properties/border-left-width)

-   [border-radius](/css/properties/border-radius)

-   [border-right](/css/properties/border-right)

-   [border-right-color](/css/properties/border-right-color)

-   [border-right-style](/css/properties/border-right-style)

-   [border-right-width](/css/properties/border-right-width)

-   [border-top](/css/properties/border-top)

-   [border-top-color](/css/properties/border-top-color)

-   **border-top-left-radius**

-   [border-top-right-radius](/css/properties/border-top-right-radius)

-   [border-top-style](/css/properties/border-top-style)

-   [border-top-width](/css/properties/border-top-width)

-   [border-width](/css/properties/border-width)
