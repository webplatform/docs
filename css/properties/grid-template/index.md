---
title: grid-template
notes:
  - 'Add description, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`See individual properties`'
  'Applies to': 'Grid containers'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'See individual properties'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: 'See indvidual properties'
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
summary: 'Shorthand for setting grid-template-columns, grid-template-rows, and grid-template-areas in a single declaration.'
tags:
  - CSS
  - Properties
uri: css/properties/grid-template

---
## <span>Summary</span>

Shorthand for setting grid-template-columns, grid-template-rows, and grid-template-areas in a single declaration.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `See individual properties`

Applies to
:   Grid containers

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   See individual properties

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   See indvidual properties

## <span>Syntax</span>

-   `grid-template: <grid-template-columns> / <grid-template-rows>`
-   `grid-template: <track-list> / <line-names> <string> <track-size> <line-names>`
-   `grid-template: none`

## <span>Values</span>

none
:   Sets all three individual properties to their initial values ("none").

\<grid-template-columns\> / \<grid-template-rows\>
:   Sets grid-template-columns and grid-template-rows to the specified values, and sets grid-template-areas to "none".

\<track-list\> / \<line-names\> \<string\> \<track-size\> \<line-names\>
:   Sets grid-template-columns to the track listing specified before the slash (or "none", if not specified). Sets grid-template-areas to the strings listed after the slash. Sets grid-template-rows to the \<track-size\>s following each string (filling in "auto" for any missing sizes), and splicing in the named lines defined before/after each size.

This syntax allows the author to align track names and sizes inline with their respective grid areas.

## <span>Examples</span>

``` css
/*
The shorthand syntax
*/
grid-template: auto 1fr auto / auto 1fr;
/*
is equivalent to
*/
grid-template-columns: auto 1fr auto;
grid-template-rows: auto 1fr;
grid-template-areas: none;
```

## <span>Related specifications</span>

[W3C Grid Layout Module](http://www.w3.org/TR/css3-grid-layout)
:   W3C Working Draft
