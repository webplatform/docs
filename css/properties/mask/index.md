---
title: mask
notes:
  - "Add description and compatibility.\nAs of time of writing, this property is not yet implemented in most browsers."
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`See individual properties.`'
  'Applies to': 'All elements. In SVG, it applies to container elements without the \<defs\> element and all graphics elements.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'See individual properties.'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: 'See individual properties.'
readiness: 'Not Ready'
standardization_status: 'W3C Last Call Working Draft'
summary: 'This property is shorthand for setting mask-image, mask-mode, mask-repeat, mask-position, mask-clip, mask-origin, mask-composite and mask-size. Omitted values are set to their original properties'' initial values.'
tags:
  - CSS
  - Properties
uri: css/properties/mask

---
## Summary

This property is shorthand for setting mask-image, mask-mode, mask-repeat, mask-position, mask-clip, mask-origin, mask-composite and mask-size. Omitted values are set to their original properties' initial values.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `See individual properties.`

Applies to
:   All elements. In SVG, it applies to container elements without the \<defs\> element and all graphics elements.

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   See individual properties.

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   See individual properties.

## Syntax

-   `mask: <mask-layer>`

## Values

\<mask-layer\>
:   Where

` <mask-layer> = <mask-reference> <masking-mode>?`

## Examples

The url points to a \<mask\> element that is used as mask.

``` css
/* mask-reference via a url */
img {
  mask: url(#masking);
}
```

``` css
/* Two mask layers (both references to mask images) that are combined with the 'add' compositing mode. */
img {
  mask: url(mask-image1.png) add, url(mask-image2.png);
}
```

## Related specifications

[CSS Masking Level 1](http://www.w3.org/TR/css-masking-1/)
:   W3C Last Call Working Draft

[CSS Masking Level 1](http://dev.w3.org/fxtf/masking/)
:   W3C Editor's Draft
