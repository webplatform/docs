---
title: line-height
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`normal`'
  'Applies to': 'all elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'for \<length\> and \<percentage\> the absolute value; otherwise as specified'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`lineHeight`'
  Percentages: 'refer to the font size of the element itself'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The line-height property specifies the height of an inline block level element. The value of the line-height property cannot be negative.'
tags:
  - CSS
  - Properties
uri: css/properties/line-height

---
## Summary

The line-height property specifies the height of an inline block level element. The value of the line-height property cannot be negative.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `normal`

Applies to
:   all elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   for \<length\> and \<percentage\> the absolute value; otherwise as specified

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `lineHeight`

Percentages
:   refer to the font size of the element itself

## Syntax

-   `line-height: <length>`
-   `line-height: <number>`
-   `line-height: <percentage>`
-   `line-height: none`
-   `line-height: normal`

## Values

normal
:   Take the height fixed by the default css of the user browser.

In most cases, it multiplies the height of the font by 1.2.

\<number\>
:   The used value of the property is this number multiplied by the element's font size. Negative values cannot be used.

\<length\>
:   The specified length is used in the calculation of the line box height: a number immediately followed by a length unit - `px`, `em`, `pc`, `in`, `mm`. Negative values cannot be used.

\<percentage\>
:   The value of this property is determined by multiplying this number by the element's font size. Negative values cannot be used.

none
:   This value has no effect on the rendering of the element and for block inline elements it is equivalent to 'normal.'

## Examples

``` css
/* setting a line-height of 1.3em to a paragraph element with a font size of 1em*/

/* with a percentage */
p { line-height: 130% }

/* with a length */
p { line-height: 1.3em}

/* with a number */
p { line-height: 1.3}
```

## Notes

### Remarks

Line height is the distance between the descender of the font and the top of the internal leading of the font. If a formatted line contains more than one object, the maximum line height applies. In this case, negative values are not allowed.

## Related specifications

[CSS1 line-height](http://www.w3.org/TR/CSS1/#line-height)
:   W3C Recommendation

[CSS2.1 line-height](http://www.w3.org/TR/CSS2/visudet.html#propdef-line-height)
:   W3C Recommendation

[css3 transition](http://dev.w3.org/csswg/css3-transitions/#animatable-css)
:   Working Draft

## See also

### Related articles

#### Box Model

-   [border](/css/properties/border)

-   [border-corner-shape](/css/properties/border-corner-shape)

-   [bottom](/css/properties/bottom)

-   [box-shadow](/css/properties/box-shadow)

-   [box-sizing](/css/properties/box-sizing)

-   [break-before](/css/properties/break-before)

-   [clear](/css/properties/clear)

-   [float](/css/properties/float)

-   [height](/css/properties/height)

-   [left](/css/properties/left)

-   **line-height**

-   [margin](/css/properties/margin)

-   [margin-bottom](/css/properties/margin-bottom)

-   [margin-left](/css/properties/margin-left)

-   [margin-right](/css/properties/margin-right)

-   [margin-top](/css/properties/margin-top)

-   [max-height](/css/properties/max-height)

-   [max-width](/css/properties/max-width)

-   [min-height](/css/properties/min-height)

-   [min-width](/css/properties/min-width)
