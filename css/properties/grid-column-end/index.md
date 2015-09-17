---
title: 'grid-column-end'
compatibility:
  feature: grid-column-end
  topic: css
notes:
  - 'Add description, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'Grid items'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
summary: 'Controls a grid item''s placement in a grid area as well as  grid position and a grid span. The grid-column-end property (with grid-row-start, grid-row-end, and grid-column-start) determines a grid item''s placement by specifying the grid lines of a grid item''s grid area.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/grid-column-end

---
## Summary

Controls a grid item's placement in a grid area as well as grid position and a grid span. The grid-column-end property (with grid-row-start, grid-row-end, and grid-column-start) determines a grid item's placement by specifying the grid lines of a grid item's grid area.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `auto`

Applies to
:   Grid items

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

-   `grid-column-end: <grid-line>`
-   `grid-column-end: <ident>`
-   `grid-column-end: <integer> <ident>`
-   `grid-column-end: auto`
-   `grid-column-end: span [ <integer> or <ident>]`

## Values

\<grid-line\>
:   Contributes a line, a span, or nothing (automatic) to the item's row placement or column placement.

auto
:   The default property that does not alter the grid item’s placement.

\<ident\>
:   Specifies that the corresponding edge of the item's grid area is the grid line at the before edge of the named grid area. If the named grid area doesn't exist, this value is treated as ‘auto’ (computing either to ‘auto’ or ‘span 1’).

\<integer\> \<ident\>
:   Contributes a line to the placement by specifying the Nth grid line. (Negative integers are allowed, but zero is not; if \<integer\> is omitted, it defaults to 1.) If a name is given as an \<ident\>, only lines with that name are counted. If no line with that name exists, it instead specifies the first grid line (or the last, if \<integer\> is negative). If not enough lines of that name exist, it specifies the last such named line (or the first, if the \<integer\> is negative).

span [ \<integer\> or \<ident\>]
:   Contributes a grid span to the placement by specifying that the corresponding edge of the item’s grid area is N grid lines from the opposite edge of the item's grid area. (Negative integers and zero are not allowed; if \<integer\> is omitted, it defaults to 1.) If a name is given as an \<ident\>, only lines with that name are counted. If no line with that name exists, the name is ignored. If not enough lines of that name exist, it spans to the last such named line.

## Examples

``` css
/* auto */
grid-column-end: auto;

/* <ident> */
grid-column-end: "C";

/* <integer> <ident> */
grid-column-end: 2 "B";

/* span <integer> */
grid-column-end: span 2;

/* span <ident> */
grid-column-end: span "C";
```

## Related specifications

[W3C Grid Layout Module](http://www.w3.org/TR/css3-grid-layout)
:   W3C Working Draft
