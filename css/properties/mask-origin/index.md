---
title: 'mask-origin'
compatibility:
  feature: mask-origin
  topic: css
notes:
  - "Add specification and compatibility.\nAs of time of writing, this property is not yet implemented in most browsers."
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`border-box`'
  'Applies to': 'All elements. In SVG, it applies to container elements without the element and all graphics elements.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified.'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
summary: 'For elements rendered as a single box, specifies the mask positioning area. For elements rendered as multiple boxes (e.g., inline boxes on several lines, boxes on several pages) specifies which boxes box-decoration-break operates on to determine the mask positioning area(s).'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/mask-origin

---
## Summary

For elements rendered as a single box, specifies the mask positioning area. For elements rendered as multiple boxes (e.g., inline boxes on several lines, boxes on several pages) specifies which boxes box-decoration-break operates on to determine the mask positioning area(s).

## Overview table

[Initial value](/css/concepts/initial_value)
:   `border-box`

Applies to
:   All elements. In SVG, it applies to container elements without the element and all graphics elements.

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

-   `mask-origin: border-box`
-   `mask-origin: content-box`
-   `mask-origin: padding-box`

## Values

padding-box
:   The position is relative to the padding box. (For single boxes, *0 0* is the upper left corner of the padding edge; *100% 100%* is the lower right corner.)

border-box
:   The position is relative to the border box (painting box for objects without associated layout box).

content-box
:   The position is relative to the content box (object bounding box for objects without associated layout box).

## Examples

``` css
/* padding-box */
body {
    background-color: white;
    mask-image: url(big-black-dot.jpg);
        mask-position: bottom right;
    mask-repeat: no-repeat;
        mask-origin: padding-box;
    }
```

Padding box

``` css
.example {
    border: 10px double;
    padding: 10px;
    -webkit-mask-image: url('mask.png');

    /* The mask image will be inside the padding */
    -webkit-mask-origin: content;
}
```

Padding box

``` css
div {
    -webkit-mask-image: url('mask1.png'), url('mask2.png');
    -webkit-mask-origin: padding, content;
}
```

## Related specifications

[CSS Masking Level 1](https://dvcs.w3.org/hg/FXTF/raw-file/default/masking/index.html)
:   W3C Editor's Draft
