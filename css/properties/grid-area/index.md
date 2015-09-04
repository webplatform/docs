---
title: grid-area
tags:
  - CSS
  - Properties
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
notes:
  - 'Add description, compatibility.'
summary: 'Lays out one or more grid items bound by 4 grid lines. Shorthand for setting grid-column-start, grid-column-end, grid-row-start, and grid-row-end in a single declaration.'
uri: css/properties/grid-area

---
# grid-area

## Summary

Lays out one or more grid items bound by 4 grid lines. Shorthand for setting grid-column-start, grid-column-end, grid-row-start, and grid-row-end in a single declaration.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `See individual properties`
Applies to
:   Grid items
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   See individual properties
Animatable
:   No
[CSS Object Model Property](/css/concepts/cssom)
:   ``
Percentages
:   See individual properties

## Syntax

-   `grid-area: <grid-line> [ <grid-line> [ <grid-line> [ <grid-line> ] ] ]`

## Values

\<grid-line\> [ \<grid-line\> [ \<grid-line\> [ \<grid-line\> ] ] ]
:   The resolution order of values for this shorthand is grid-row-start, grid-column-start, grid-row-end, grid-column-end. That is, if four \<grid-line\> values are specified, grid-row-start is set to the first value, grid-column-start is set to the second value, grid-row-end is set to the third value, and grid-column-end is set to the fourth value.

When grid-column-end is omitted, if grid-column-start is an \<ident\>, grid-column-end is set to that \<ident\>; otherwise, it is set to auto.

When grid-row-end is omitted, if grid-row-start is an \<ident\>, grid-row-end is set to that \<ident\>; otherwise, it is set to auto.

When grid-column-start is omitted, if grid-row-start is an \<ident\>, all four longhands are set to that value. Otherwise, it is set to auto.

## Examples

``` {.css}
grid-area: 1 2 2 3;

/*  Equivalent to :

grid-row-start: 1
grid-column-start: 2
grid-row-end: 2;
grid-column-end: 3;

*/
```

## Related specifications

Specification
:   Status
[W3C Grid Layout Module](http://www.w3.org/TR/css3-grid-layout)
:   W3C Working Draft

