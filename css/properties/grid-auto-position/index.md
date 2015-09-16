---
title: grid-auto-position
notes:
  - 'Add description, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`1 / 1`'
  'Applies to': 'Grid containers'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
summary: 'Specifies the automatic default location if a grid container does not specify automatic-placement strategy via grid-auto-flow.'
tags:
  - CSS
  - Properties
uri: css/properties/grid-auto-position

---
## Summary

Specifies the automatic default location if a grid container does not specify automatic-placement strategy via grid-auto-flow.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `1 / 1`

Applies to
:   Grid containers

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

-   `grid-auto-position: <grid-line> / <grid-line>`

## Values

\<grid-line\> / \<grid-line\>
:   Specifies the default starting grid column and grid row, respectively. The two \<grid-line\> values are treated as though they were specified by [grid-column-start](/css/properties/grid-column-start) and [grid-column-end](/css/properties/grid-column-end).

## Examples

``` css
/*
This example specifies that (not otherwise placed) grid items
will be placed at column 1, row 2.
*/
#grid{
    grid-auto-position: 1 / 2;
  }
```

## Related specifications

[W3C Grid Layout Module](http://www.w3.org/TR/css3-grid-layout)
:   W3C Working Draft
