---
title: grid-template-columns
notes:
  - 'Add description, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'grid containers'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified, except for "auto"'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
summary: 'Specifies (with grid-template-rows) the line names and track sizing functions of the grid. Each sizing function can be specified as a length, a percentage of the grid container’s size, a measurement of the contents occupying the column or row, or a fraction of the free space in the grid.'
tags:
  - CSS
  - Properties
uri: css/properties/grid-template-columns

---
## <span>Summary</span>

Specifies (with grid-template-rows) the line names and track sizing functions of the grid. Each sizing function can be specified as a length, a percentage of the grid container’s size, a measurement of the contents occupying the column or row, or a fraction of the free space in the grid.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `none`

Applies to
:   grid containers

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified, except for "auto"

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   N/A

## <span>Syntax</span>

-   `grid-template-columns: <track-list>`
-   `grid-template-columns: none`
-   `grid-template-columns: subgrid <line-name-list>`

## <span>Values</span>

none
:   Indicates that there is no explicit grid; any rows/columns will be implicitly generated, and their size will be determined by the grid-auto-rows and grid-auto-columns properties.

\<track-list\>
:   Specifies the track list for the grid columns. See [specification](http://www.w3.org/TR/css3-grid-layout/#track-list) for complete syntax.

subgrid \<line-name-list\>
:   Indicates that the grid will align to its parent grid in that axis. Rather than specifying the sizes of rows/columns explicitly, they will be taken from the parent grid’s definition. If the grid container is not a grid item, this value computes to "none".

## <span>Examples</span>

``` css
grid-template-columns: 100px 1fr max-content minmax(min-content, 1fr);
/* Creates five grid lines:
1. At the start edge of the grid container
2. 100px from the start edge of the grid container
3. At a distance from the previous line equal to half the free space
   (the width of the grid container minus the width of the non-flexible grid tracks)
4. At a distance from the previous line equal to the maximum size of any grid items
   belonging to the column between these two lines
5. At a distance from the previous line at least as large as the largest minimum size of any grid items
   belonging to the column between these two lines, but no larger than the other half of the free space
*/
```

## <span>Related specifications</span>

[CSS Grid Layout Module Level 1](http://www.w3.org/TR/css3-grid-layout/)
:   W3C Working Draft
