---
title: mask-clip
notes:
  - "Add description and compatibility.\nAs of time of writing, this property is not yet implemented in most browsers."
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`border-box`'
  'Applies to': 'All elements. In SVG, it applies to container elements without the \<defs\> element and all graphics elements.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified.'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
summary: 'Determines the mask painting area, which defines the area that is affected by the mask. The painted content of an element may be restricted to this area.'
tags:
  - CSS
  - Properties
uri: css/properties/mask-clip

---
## Summary

Determines the mask painting area, which defines the area that is affected by the mask. The painted content of an element may be restricted to this area.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `border-box`

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

-   `mask-clip: border-box`
-   `mask-clip: content-box`
-   `mask-clip: no-clip`
-   `mask-clip: padding-box`

## Values

no-clip
:   The painted content is not restricted (not clipped). The mask painting area is set to the bounding client rect.

border-box
:   The painted content is restricted (clipped) to the border box (painting box for objects without associated layout box).

padding-box
:   The painted content is restricted (clipped) to the padding box.

content-box
:   The painted content is restricted (clipped) to the content box (object bounding box for objects without associated layout box).

## Examples

``` css
/* border-box */
body {
    background-color: white;
    mask-image: url(big-black-dot.jpg);
        mask-position: bottom right;
    mask-repeat: no-repeat;
        mask-clip: border-box;
    }
```

## Related specifications

[CSS Masking Level 1](http://www.w3.org/TR/css-masking/)
:   W3C Working Draft
