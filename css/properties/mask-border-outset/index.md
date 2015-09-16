---
title: 'mask-border-outset'
compatibility:
  feature: mask-border-outset
  topic: css
notes:
  - "Add description and compatibility.\nAs of time of writing, this property is not yet implemented in most browsers."
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`0`'
  'Applies to': 'All elements. In SVG, it applies to container elements without the \<defs\> element and all graphics elements.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'All \<length\>s made absolute, otherwise as specified.'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'In Progress'
standardization_status: 'W3C Last Call Working Draft'
summary: 'This property specifies the amount by which the mask box image area extends beyond the border box, similar to the CSS border-image-outset property. The four values set the outsets on the top, right, bottom, and left sides in that order.'
tags:
  - CSS
  - Properties
uri: css/properties/mask-border-outset

---
## Summary

This property specifies the amount by which the mask box image area extends beyond the border box, similar to the CSS border-image-outset property. The four values set the outsets on the top, right, bottom, and left sides in that order.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `0`

Applies to
:   All elements. In SVG, it applies to container elements without the \<defs\> element and all graphics elements.

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   All \<length\>s made absolute, otherwise as specified.

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   N/A

## Syntax

-   `mask-border-outset: length`
-   `mask-border-outset: number`

## Values

length
:   Represents pixels if the image is a raster image or vector coordinates if the image is a vector image.

number
:   Represents multiples of the corresponding computed *border-width*.

## Examples

``` css
/* length */
#maskbox1: {
    mask-border-outset: 30 50 30 50;
}
```

## Related specifications

[CSS Masking Level 1](http://www.w3.org/TR/css-masking-1/)
:   W3C Last Call Working Draft

[CSS Masking Level 1](http://dev.w3.org/fxtf/css-masking-1/)
:   W3C Editor’s Draft
