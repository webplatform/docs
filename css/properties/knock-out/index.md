---
title: 'knock-out'
compatibility:
  feature: knock-out
  topic: css
notes:
  - 'Add description, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`preserve`'
  'Applies to': 'All HTML elements. In SVG, it applies to all container elements except *mask*.'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified.'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
summary: 'Defines whether an element group is a knock-out group. When a group is set to knock-out, the elements in the group only composite and blend with elements outside the group. When a group is set to preserve (the default), the elements composite normally and blend with other elements inside and outside the group.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/knock-out

---
## Summary

Defines whether an element group is a knock-out group. When a group is set to knock-out, the elements in the group only composite and blend with elements outside the group. When a group is set to preserve (the default), the elements composite normally and blend with other elements inside and outside the group.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `preserve`

Applies to
:   All HTML elements. In SVG, it applies to all container elements except *mask*.

[Inherited](/css/concepts/inherited)
:   Yes

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

-   `knock-out: knock-out`
-   `knock-out: preserve`

## Values

preserve
:   Elements in the group composite normally and blend with other elements inside and outside the group.

knock-out
:   Elements in the group only composite and blend with elements outside the group.

## Examples

``` css
/* knock-out */
div.ko {
    knock-out: knock-out;
}
```

## Related specifications

[Compositing and Blending Level 1](http://dev.w3.org/fxtf/compositing-1)
:   W3C Editor's Draft

[Compositing and Blending 1.0](http://www.w3.org/TR/2012/WD-compositing-20120816)
:   W3C Working Draft
