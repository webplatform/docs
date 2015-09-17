---
title: 'mask-type'
compatibility:
  feature: mask-type
  topic: css
notes:
  - "Add specification and compatibility.\nAs of time of writing, this property is not yet implemented in most browsers."
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`luminance`'
  'Applies to': '\<mask\> elements.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'the unique non-ambiguous order defined by the formal grammar'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'In Progress'
standardization_status: 'W3C Last Call Working Draft'
summary: 'Defines whether the content of the &lt;mask&gt; element is treated as as luminance mask or an alpha mask.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/mask-type

---
## Summary

Defines whether the content of the &lt;mask&gt; element is treated as as luminance mask or an alpha mask.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `luminance`

Applies to
:   \<mask\> elements.

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   the unique non-ambiguous order defined by the formal grammar

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   N/A

## Syntax

-   `mask-type: alpha`
-   `mask-type: luminance`

## Values

luminance
:   Indicates that the luminance values of the mask should be used.

alpha
:   Indicates that the alpha values of the mask should be used.

## Examples

Alpha mask type

``` html
<mask style="mask-type: alpha">
        <circle cx="50%" cy="50%" r="50%"/>
</mask>
```

Luminance mask type

``` css
<mask style="mask-type: luminance">
        <circle cx="50%" cy="50%" r="50%" fill="white"/>
</mask>
```

## Related specifications

[CSS Masking Level 1](http://www.w3.org/TR/css-masking-1/)
:   W3C Last Call Working Draft

[CSS Masking Level 1](http://dev.w3.org/fxtf/css-masking-1/)
:   W3C Editor’s Draft
