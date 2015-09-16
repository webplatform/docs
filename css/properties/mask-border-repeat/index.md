---
title: 'mask-border-repeat'
compatibility:
  feature: mask-border-repeat
  topic: css
notes:
  - "Add description and compatibility.\nAs of time of writing, this property is not yet implemented in most browsers."
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`stretch`'
  'Applies to': 'All elements. In SVG, it applies to container elements without the \<defs\> element and all graphics elements.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'In Progress'
standardization_status: 'W3C Last Call Working Draft'
summary: 'This property specifies how the images for the sides and the middle part of the mask image are scaled and tiled. The first keyword applies to the horizontal sides, the second one applies to the vertical ones. If the second keyword is absent, it is assumed to be the same as the first, similar to the CSS border-image-repeat property.'
tags:
  - CSS
  - Properties
uri: css/properties/mask-border-repeat

---
## Summary

This property specifies how the images for the sides and the middle part of the mask image are scaled and tiled. The first keyword applies to the horizontal sides, the second one applies to the vertical ones. If the second keyword is absent, it is assumed to be the same as the first, similar to the CSS border-image-repeat property.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `stretch`

Applies to
:   All elements. In SVG, it applies to container elements without the \<defs\> element and all graphics elements.

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   N/A

## Syntax

-   `mask-border-repeat: repeat`
-   `mask-border-repeat: round`
-   `mask-border-repeat: space`
-   `mask-border-repeat: stretch`

## Values

stretch
:   The image is stretched to fill the area.

repeat
:   The image is tiled (repeated) to fill the area.

round
:   The image is tiled (repeated) to fill the area. If it does not fill the area with a whole number of tiles, the image is rescaled so that it does.

space
:   The image is tiled (repeated) to fill the area. If it does not fill the area with a whole number of tiles, the extra space is distributed around the tiles.

## Examples

``` css
/* explicit horizontal, explicit vertical */
#maskbox1: {
    mask-border-repeat: stretch repeat;
}

/* explicit horizontal, implicit vertical */
#maskbox1: {
    mask-border-repeat: round;
}
```

## Related specifications

[CSS Masking Level 1](http://www.w3.org/TR/css-masking-1/)
:   W3C Last Call Working Draft

[CSS Masking Level 1](http://dev.w3.org/fxtf/css-masking-1/)
:   W3C Editor’s Draft
