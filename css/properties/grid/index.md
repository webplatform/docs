---
title: grid
tags:
  - CSS
  - Properties
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
notes:
  - 'Add description, specifications, compatibility.'
summary: 'Foundation of a two-dimensional grid-based layout system.  Defines an element as part of a grid and permits those elements to be displayed differently than the flow order.  Also used as a shorthand for setting all the explicit grid properties (grid-template-rows, grid-template-columns, and grid-template-areas), as well as all the implicit grid properties (grid-auto-rows, grid-auto-columns, and grid-auto-flow), in a single declaration. If the <grid-auto-rows> value is omitted, it is set to the value specified for grid-auto-columns. Other omitted values are set to their initial values.'
uri: css/properties/grid

---
# grid

## Summary

Foundation of a two-dimensional grid-based layout system. Defines an element as part of a grid and permits those elements to be displayed differently than the flow order. Also used as a shorthand for setting all the explicit grid properties (grid-template-rows, grid-template-columns, and grid-template-areas), as well as all the implicit grid properties (grid-auto-rows, grid-auto-columns, and grid-auto-flow), in a single declaration. If the \<grid-auto-rows\> value is omitted, it is set to the value specified for grid-auto-columns. Other omitted values are set to their initial values.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `See individual properties`
Applies to
:   Grid containers, Grid layout
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

-   `grid: <grid-auto-columns> / <grid-auto-rows>`
-   `grid: <grid-auto-flow>`
-   `grid: <grid-template>`

## Values

\<grid-template\>
:   Itself a shorthand property, see [grid-template](/css/properties/grid-template) for details.

\<grid-auto-flow\>
:   See [grid-auto-flow](/css/properties/grid-auto-flow) for details.

\<grid-auto-columns\> / \<grid-auto-rows\>
:   See [grid-auto-columns](/css/properties/grid-auto-columns) and [grid-auto-rows](/css/properties/grid-auto-rows) for details.

## Examples

``` {.css}
#grid {
      display: grid;
      grid-template-columns: auto minmax(min-content, 1fr);
          grid-template-rows: auto minmax(min-content, 1fr) auto
  }
  #prdName    { grid-column: 1; grid-row: 1 }
  #grossPrice    { grid-column: 1; grid-row: 3 }
  #retailPrice   { grid-column: 1; grid-row: 2; justify-self: start }
  #discount    { grid-column: 2; grid-row: 1 / span 2; }
  #finalPrice { grid-column: 2; grid-row: 3; align-self: center}
```

