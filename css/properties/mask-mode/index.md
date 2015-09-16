---
title: 'mask-mode'
compatibility:
  feature: mask-mode
  topic: css
notes:
  - "Add specification and compatibility.\nAs of time of writing, this property is not yet implemented in most browsers."
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'All elements. In SVG, it applies to container elements without the \<defs\> element and all graphics elements.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified.'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
summary: 'This property indicates whether the &lt;mask-reference&gt; is treated as a luminescence mask or as an alpha mask.'
tags:
  - CSS
  - Properties
uri: css/properties/mask-mode

---
## Summary

This property indicates whether the &lt;mask-reference&gt; is treated as a luminescence mask or as an alpha mask.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `auto`

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
:

Percentages
:   N/A

## Syntax

-   `mask-mode: alpha`
-   `mask-mode: auto`
-   `mask-mode: luminance`

## Values

auto
:   Implicitly sets alpha or luminance, depending on the \<mask-reference\> value of the mask-image property. If it is of type \<mask-source\>, the luminance values of the mask image should be used as the mask values; if it is of type \<image\>, the alpha values of the mask image should be used as the mask values.

alpha
:   Indicates that the alpha values of the mask image should be used as the mask values.

luminance
:   Indicates that the luminance values of the mask image should be used as the mask values.

## Examples

``` css
/* auto */
#img1 {
    mask-source-type: auto;
  }

/* alpha */
#img2 {
    mask-source-type: alpha;
  }

/* luminance */
#img3 {
    mask-source-type: luminance;
  }
```

## Related specifications

[CSS Masking Level 1](https://dvcs.w3.org/hg/FXTF/raw-file/default/masking/index.html)
:   W3C Editor's Draft
