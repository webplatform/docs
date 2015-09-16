---
title: mask-position
notes:
  - "Add specification and compatibility.\nAs of time of writing, this property is not yet implemented in most browsers."
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`center`'
  'Applies to': 'All elements. In SVG, it applies to container elements without the \<defs\> element and all graphics elements.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'Two keywords representing the origin and two offsets from that origin, each given as an absolute length (if given a \<length\>), otherwise as a percentage.'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: 'Refer to size of mask painting area minus size of mask image.'
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
summary: 'This property sets the initial position of a mask image. Position can be specified in terms of percentages of the distance from upper left corner (original point) or using the keywords top, left, center, right, or bottom, similar to the CSS background-position property.'
tags:
  - CSS
  - Properties
uri: css/properties/mask-position

---
## Summary

This property sets the initial position of a mask image. Position can be specified in terms of percentages of the distance from upper left corner (original point) or using the keywords top, left, center, right, or bottom, similar to the CSS background-position property.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `center`

Applies to
:   All elements. In SVG, it applies to container elements without the \<defs\> element and all graphics elements.

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   Two keywords representing the origin and two offsets from that origin, each given as an absolute length (if given a \<length\>), otherwise as a percentage.

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   Refer to size of mask painting area minus size of mask image.

## Syntax

-   `mask-position: length length`
-   `mask-position: percentage percentage`
-   `mask-position: percentage`
-   `mask-position: bottom length right length`
-   `mask-position: left top`

## Values

[length](/css/data_types/length) [length](/css/data_types/length)
:   Any standard CSS units are acceptable as `mask-position` values: px, ems, rems, mm, cm etc. Note that unit values specify the distance the top left corner of the mask is away from the top left corner of the element. For more details on these units, read [Length units](/css/data_types/length).

[percentage](/css/data_types/percentage) [percentage](/css/data_types/percentage)
:   Percentages are acceptable for `mask-position` values, and specify percentages of the overall width and height of the element in question. Note that percentage values specify the distance the top left corner of the mask is away from the top left corner of the element.

left top
:   `mask-position` can also be expressed as keywords: left top, top, right top, left, center, right, left bottom, bottom, right bottom. These values do not relate specifically to the position of the top left hand corner of the mask, but rather the overall position of the mask inside the element. So for example, a value of `right top` will make the right and top sides of the mask flush to the top and right sides of the element it is applied to; the top left corner *won't* be positioned at the top right of the element!

[percentage](/css/data_types/percentage)
:   If only a single value is included, that is taken as the horizontal value, and the vertical value is set as `center`.

bottom [length](/css/data_types/length) right [length](/css/data_types/length)
:   CSS3 includes the new four value `mask-position` syntax, which allows you to choose which sides of the element you are positioning the mask relative to (values 1 and 3), and then the distance away from those sides (values 2 and 4). So this example says that you want to position the mask 10 pixels from the bottom of the element, and 15 pixels from the right. If you miss out one of the offset values, the other is assumed to be 0.

## Examples

``` css
/* bottom right */
body {
    background-color: white;
    mask-image: url(big-black-dot.jpg);
        mask-position: bottom right;
    mask-repeat: no-repeat;
    }
```

## Related specifications

[CSS Masking Level 1](https://dvcs.w3.org/hg/FXTF/raw-file/default/masking/index.html)
:   W3C Editor's Draft
