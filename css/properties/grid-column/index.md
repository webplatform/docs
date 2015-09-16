---
title: grid-column
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - "Add description, compatibility.\nPreviously imported as ms-grid-column."
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`See individual properties`'
  'Applies to': 'Grid items'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'See individual properties'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: 'See individual properties'
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
summary: 'Controls a grid item''s placement in a grid area, particularly grid position and a grid span.   Shorthand for setting grid-column-start and grid-column-end in a single declaration.'
tags:
  - CSS
  - Properties
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - css/properties/ms-grid-columns
    - css/properties/ms-grid-row
uri: css/properties/grid-column

---
## Summary

Controls a grid item's placement in a grid area, particularly grid position and a grid span. Shorthand for setting grid-column-start and grid-column-end in a single declaration.

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
:

Percentages
:   See individual properties

## Syntax

-   `grid-column: <grid-line> [ / <grid-line> ]`

## Values

\<grid-line\> [ / \<grid-line\> ]
:   If two \<grid-line\> values are specified, the grid-column-start property is set to the value before the slash, and the grid-column-end property is set to the value after the slash. If the second value is omitted, then if the first value is an identifier (\<ident\>), the grid-column-end property is also set to that \<ident\>; otherwise, it is set to "auto".

## Examples

``` css
/*
The shorthand syntax
*/
grid-column: 1 / 3;
/*
is equivalent to
*/
grid-column-start: 1
grid-column-end: 3;
```

## Related specifications

[W3C Grid Layout Module](http://www.w3.org/TR/css3-grid-layout)
:   W3C Working Draft

## See also

### Related pages (MSDN)

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `style`
-   `a`
-   `abbr`
-   `acronym`
-   `b`
-   `bdo`
-   `big`
-   `br`
-   `cite`
-   `code`
-   `dfn`
-   `em`
-   `i`
-   `img`
-   `input`
-   `kbd`
-   `label`
-   `q`
-   `samp`
-   `select`
-   `small`
-   `span`
-   `strong`
-   `sub`
-   `sup`
-   `textArea`
-   `tt`
-   `var`
-   `address`
-   `blockQuote`
-   `div`
-   `dl`
-   `fieldSet`
-   `form`
-   `noFrames`
-   `noScript`
-   `ol`
-   `p`
-   `pre`
-   `table`
-   `ul`
-   `dd`
-   `dt`
-   `li`
-   `tBody`
-   `td`
-   `tFoot`
-   `th`
-   `tHead`
-   `tr`
-   `button`
-   `del`
-   `ins`
-   `map`
-   `object`
-   `script`
-   `-ms-grid-columns`
-   `-ms-grid-row`
