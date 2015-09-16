---
title: 'mask-repeat'
compatibility:
  feature: mask-repeat
  topic: css
notes:
  - "Add specification and compatibility.\nAs of time of writing, this property is not yet implemented in most browsers."
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`no-repeat`'
  'Applies to': 'All elements. In SVG, it applies to container elements without the \<defs\> element and all graphics elements.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'Two keywords, one per dimension'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
summary: 'Specifies how mask images are tiled (repeated) after they have been sized and positioned.'
tags:
  - CSS
  - Properties
uri: css/properties/mask-repeat

---
## Summary

Specifies how mask images are tiled (repeated) after they have been sized and positioned.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `no-repeat`

Applies to
:   All elements. In SVG, it applies to container elements without the \<defs\> element and all graphics elements.

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   Two keywords, one per dimension

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   N/A

## Syntax

-   `mask-repeat: no-repeat`
-   `mask-repeat: repeat`
-   `mask-repeat: repeat-x`
-   `mask-repeat: repeat-y`
-   `mask-repeat: round`
-   `mask-repeat: space`

## Values

repeat-x
:   Tiling of the mask object occurs in the x direction.

repeat-y
:   Tiling of the mask object occurs in the y direction.

repeat
:   Tiling of the mask object occurs in both the x and y directions as often as needed to cover the background area.

space
:   Tiling of the mask object occurs in both the x and y directions as often as will fit within the background positioning area without being clipped, and then the images are spaced out to fill the area.

round
:   Tiling of the mask object occurs in both the x and y directions as often as will fit within the background positioning area. If it does not fit a whole number of times, it is rescaled so that it does.

no-repeat
:   Tiling of the mask object does not occur; that is, it is placed once and not repeated.

## Examples

``` css
/* repeat-y */
body {
  background-color: white;
  mask-image: url(dot-mask.png);
  mask-position: center;
  mask-repeat: repeat-y;
}
```

## Related specifications

[CSS Masking Level 1](https://dvcs.w3.org/hg/FXTF/raw-file/default/masking/index.html)
:   W3C Editor's Draft
