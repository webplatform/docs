---
title: grid-row
tags:
  - CSS
  - Properties
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
notes:
  - 'Add description, compatibility.'
summary: 'Gets or sets a value that indicates which row an element within a Grid should appear in.  Shorthand for setting grid-row-start and grid-row-end in a single declaration.'
uri: css/properties/grid-row

---
# grid-row

## Summary

Gets or sets a value that indicates which row an element within a Grid should appear in. Shorthand for setting grid-row-start and grid-row-end in a single declaration.

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

-   `grid-row: <grid-line> [ / <grid-line> ]`

## Values

\<grid-line\> [ / \<grid-line\> ]
:   If two \<grid-line\> values are specified, the grid-row-start property is set to the value before the slash, and the grid-row-end property is set to the value after the slash.

When the second value is omitted, then if the first value is an identifier (\<ident\>), the grid-row-end property is also set to that \<ident\>; otherwise, it is set to "auto".

## Examples

``` {.css}
/*
The shorthand syntax
*/
grid-row: 1 / 3;
/*
is equivalent to
*/
grid-row-start: 1
grid-row-end: 3;
```

## Related specifications

Specification
:   Status
[W3C Grid Layout Module](http://www.w3.org/TR/css3-grid-layout)
:   W3C Working Draft

