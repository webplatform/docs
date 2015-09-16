---
title: grid-row-start
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
summary: 'A grid item''s placement in a grid area consists of a grid position and a grid span. The grid-row-start property (with grid-row-end, grid-column-start, and grid-column-end) determines a grid item''s placement by specifying the grid lines of a grid item''s grid area.'
tags:
  - CSS
  - Properties
uri: css/properties/grid-row-start

---
## Summary

A grid item's placement in a grid area consists of a grid position and a grid span. The grid-row-start property (with grid-row-end, grid-column-start, and grid-column-end) determines a grid item's placement by specifying the grid lines of a grid item's grid area.

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

-   `grid-row-start: <grid-line>`

## Values

\<grid-line\>
:   Contributes a line, a span, or nothing (automatic) to the item's row placement or column placement. Values have the following meanings:

-   **auto** - The property contributes nothing to the grid item’s placement.
-   **\<ident\>** - If there is a named grid area with the specified name, contributes a line to the placement by specifying the line at the corresponding edge of that named grid area. Otherwise, if there is a named line with the specified name, contributes a line to the placement by specifying the first line of that name. Otherwise, contributes nothing to the placement.
-   **\<integer\> \<ident\>** - Contributes a line to the placement by specifying the Nth grid line. (Negative integers are allowed, but zero is not; if \<integer\> is omitted, it defaults to 1.) If a name is given as an \<ident\>, only lines with that name are counted. If no line with that name exists, it instead specifies the first grid line (or the last, if \<integer\> is negative). If not enough lines of that name exist, it specifies the last such named line (or the first, if the \<integer\> is negative).
-   **span** [ **\<integer\>** *or* **\<ident\>** ] - Contributes a grid span to the placement by specifying that the corresponding edge of the item’s grid area is N grid lines from the opposite edge of the item's grid area. (Negative integers and zero are not allowed; if \<integer\> is omitted, it defaults to 1.) If a name is given as an \<ident\>, only lines with that name are counted. If no line with that name exists, the name is ignored. If not enough lines of that name exist, it spans to the last such named line.

## Examples

``` css
/* auto */
grid-row-start: auto;

/* <ident> */
grid-row-start: "C";

/* <integer> <ident> */
grid-row-start: 2 "B";

/* span <integer> */
grid-row-start: span 2;

/* span <ident> */
grid-row-start: span "C";
```

## Related specifications

[W3C Grid Layout Module](http://www.w3.org/TR/css3-grid-layout)
:   W3C Working Draft
