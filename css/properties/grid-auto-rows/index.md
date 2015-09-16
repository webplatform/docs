---
title: grid-auto-rows
notes:
  - 'Add description, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'Grid containers'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: 'As specified'
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
summary: 'Changes default size of grid rows.  Creates implicit grid tracks when a grid item is placed into a row that is not explicitly sized (by grid-template-rows ) or when the auto-placement algorithm has generated additional rows. This property (with grid-auto-columns) specifies the size of such implicitly-created tracks.'
tags:
  - CSS
  - Properties
uri: css/properties/grid-auto-rows

---
## Summary

Changes default size of grid rows. Creates implicit grid tracks when a grid item is placed into a row that is not explicitly sized (by grid-template-rows ) or when the auto-placement algorithm has generated additional rows. This property (with grid-auto-columns) specifies the size of such implicitly-created tracks.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `auto`

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
:   As specified

## Syntax

-   `grid-auto-rows: <track-size>`

## Values

\<track-size\>
:   A space-separated track list specifying the line names and track sizing functions of the grid.

## Examples

``` css
/*
In this example, grid item B is positioned in column 5,
which creates four implicit columns (1-4) and one implicit row (2).
The implicit (auto) columns and rows are sized at 20px
using grid-auto-columns and grid-column-rows.
*/
<style type="text/css">
  #grid {
display: grid;
grid-auto-columns: 20px;
grid-auto-rows: 20px }
  #A { grid-column: 1;          grid-row: 1; }
  #B { grid-column: 5;          grid-row: 1 / span 2; }
  #C { grid-column: 1 / span 2; grid-row: 2; }
</style>
```

## Related specifications

[W3C Grid Layout Module](http://www.w3.org/TR/css3-grid-layout)
:   W3C Working Draft

## See also

### Related articles

#### CSS Layout

-   [Responsive Web Design](/concepts/mobile_web/responsive_design)

-   [@import](/css/atrules/@import)

-   [align-self](/css/properties/align-self)

-   [background](/css/properties/background)

-   [box-decoration-break](/css/properties/box-decoration-break)

-   [box-flex](/css/properties/box-flex)

-   [box-lines](/css/properties/box-lines)

-   [box-orient](/css/properties/box-orient)

-   [box-pack](/css/properties/box-pack)

-   [box-shadow](/css/properties/box-shadow)

-   [break-before](/css/properties/break-before)

-   [flex-align](/css/properties/flex-align)

-   [flex-item-align](/css/properties/flex-item-align)

-   [flex-line-pack](/css/properties/flex-line-pack)

-   **grid-auto-rows**

-   [grid-definition-columns](/css/properties/grid-definition-columns)

-   [grid-definition-rows](/css/properties/grid-definition-rows)

-   [height](/css/properties/height)

-   [max-width](/css/properties/max-width)

-   [user-modify](/css/properties/user-modify)

-   [baseline-shift](/svg/attributes/baseline-shift)

#### Grid Layout

-   [Responsive Web Design](/concepts/mobile_web/responsive_design)

-   **grid-auto-rows**

-   [grid-column-position](/css/properties/grid-column-position)

-   [grid-column-span](/css/properties/grid-column-span)

-   [grid-definition-columns](/css/properties/grid-definition-columns)

-   [grid-definition-rows](/css/properties/grid-definition-rows)

-   [grid-row-position](/css/properties/grid-row-position)

-   [height](/css/properties/height)
