---
title: 'grid-template'
compatibility:
  feature: grid-template
  topic: css
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
  - CSS_Properties
  - CSS
uri: css/properties/grid-template

---
## Summary

Shorthand for setting grid-template-columns, grid-template-rows, and grid-template-areas in a single declaration.

## Overview table

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

## Syntax

-   `grid-template: <grid-template-columns> / <grid-template-rows>`
-   `grid-template: <track-list> / <line-names> <string> <track-size> <line-names>`
-   `grid-template: none`

## Values

none
:   Sets all three individual properties to their initial values ("none").

\<grid-template-columns\> / \<grid-template-rows\>
:   Sets grid-template-columns and grid-template-rows to the specified values, and sets grid-template-areas to "none".

\<track-list\> / \<line-names\> \<string\> \<track-size\> \<line-names\>
:   Sets grid-template-columns to the track listing specified before the slash (or "none", if not specified). Sets grid-template-areas to the strings listed after the slash. Sets grid-template-rows to the \<track-size\>s following each string (filling in "auto" for any missing sizes), and splicing in the named lines defined before/after each size.

This syntax allows the author to align track names and sizes inline with their respective grid areas.

## Examples

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

## Related specifications

[W3C Grid Layout Module](http://www.w3.org/TR/css3-grid-layout)
:   W3C Working Draft
