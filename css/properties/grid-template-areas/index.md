---
title: grid-template-areas
notes:
  - 'Add description, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'Grid containers'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
summary: 'Specifies named grid areas which are not associated with any particular grid item, but can be referenced from the grid-placement properties. The syntax of the grid-template-areas property also provides a visualization of the structure of the grid, making the overall layout of the grid container easier to understand.'
tags:
  - CSS
  - Properties
uri: css/properties/grid-template-areas

---
## <span>Summary</span>

Specifies named grid areas which are not associated with any particular grid item, but can be referenced from the grid-placement properties. The syntax of the grid-template-areas property also provides a visualization of the structure of the grid, making the overall layout of the grid container easier to understand.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `none`

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

## <span>Syntax</span>

-   `grid-template-areas: <string>`
-   `grid-template-areas: none`

## <span>Values</span>

none
:   The grid container does not define any named grid areas.

\<string\>
:   A row is created for every separate string listed, and a column is created for each identifier or period (".") in the string. A period represents an unnamed area in the grid container. An identifier creates a named grid area with the identifier as its name.

## <span>Examples</span>

``` css
/*
Creates a page layout where areas are defined for header content (head),
navigational content (nav), footer content (foot), and main content (main).
Accordingly, the template creates three rows and two columns, with four named grid areas.
The head area spans both columns in the first row of the grid.
*/

<style type="text/css">
  #grid {
    display: grid;
    grid-template-areas: "head head"
                         "nav  main"
                         "foot .   "
  }
  #grid > header { grid-area: head; }
  #grid > nav    { grid-area: nav; }
  #grid > main   { grid-area: main; }
  #grid > footer { grid-area: foot; }
</style>
```

## <span>Related specifications</span>

[W3C Grid Layout Module](http://www.w3.org/TR/css3-grid-layout)
:   W3C Working Draft
