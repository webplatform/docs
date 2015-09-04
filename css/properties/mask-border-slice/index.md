---
title: mask-border-slice
tags:
  - CSS
  - Properties
readiness: 'In Progress'
standardization_status: 'W3C Last Call Working Draft'
notes:
  - "Add description and compatibility.\nAs of time of writing, this property is not yet implemented in most browsers."
summary: 'This property specifies inward offsets from the top, right, bottom, and left edges of the mask image, dividing it into nine regions: four corners, four edges, and a middle. The middle image part is discarded and treated as fully transparent black unless the fill keyword is present. The four values set the top, right, bottom and left offsets in that order, similar to the CSS border-image-slice property.'
uri: css/properties/mask-border-slice

---
# mask-border-slice

## Summary

This property specifies inward offsets from the top, right, bottom, and left edges of the mask image, dividing it into nine regions: four corners, four edges, and a middle. The middle image part is discarded and treated as fully transparent black unless the fill keyword is present. The four values set the top, right, bottom and left offsets in that order, similar to the CSS border-image-slice property.

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
:   As specified.
Animatable
:   No
[CSS Object Model Property](/css/concepts/cssom)
:   ``
Percentages
:   Refer to the size of the mask image.

## Syntax

-   `mask-border-slice: <number>`
-   `mask-border-slice: <percentage>`
-   `mask-border-slice: fill`

## Values

\<percentage\>
:   Refers to the size of the mask box image area: the width of the area for horizontal offsets, the height for vertical offsets.

\<number\>
:   Represents pixels if the image is a raster image or vector coordinates if the image is a vector image.

fill
:   If present, causes the middle part of the mask image to be preserved. If omitted, the middle part of the mask image is discarded, i.e., treated as empty.

## Examples

``` {.css}
/* numbers, fill */
#maskbox1: {
    mask-border-slice: 30 50 30 50 fill;
}

/* percentages, no fill */
#maskbox2: {
    mask-border-slice: 25% 10% 20% 25%;
}
```

## Related specifications

Specification
:   Status
[CSS Masking Level 1](http://www.w3.org/TR/css-masking-1/)
:   W3C Last Call Working Draft
[CSS Masking Level 1](http://dev.w3.org/fxtf/css-masking-1/)
:   W3C Editor’s Draft

