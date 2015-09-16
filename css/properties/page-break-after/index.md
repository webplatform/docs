---
title: 'page-break-after'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: page-break-after
  topic: css
notes:
  - 'Deprecated; deletion candidate'
overview_table:
  '[Initial value](/css/concepts/initial_value)': ''
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'Not Ready'
standardization_status: Deprecated
summary: 'The page-break-after property is supported in all major browsers. With CSS3, page-break-* properties are only aliases of the break-* properties. The CSS3 Fragmentation spec defines breaks for all CSS box fragmentation.'
tags:
  - CSS
  - Properties
uri: css/properties/page-break-after

---
## Summary

The page-break-after property is supported in all major browsers. With CSS3, page-break-\* properties are only aliases of the break-\* properties. The CSS3 Fragmentation spec defines breaks for all CSS box fragmentation.

## Overview table

[Initial value](/css/concepts/initial_value)
:

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

## Syntax

-   `page-break-after: always`
-   `page-break-after: auto`
-   `page-break-after: avoid`
-   `page-break-after: empty string`
-   `page-break-after: inherit`
-   `page-break-after: left`
-   `page-break-after: right`

## Values

auto
:   Default. Insert a page break after the element if necessary

always
:   Insert a page break after the element

avoid
:   Avoid inserting a page break after the element

empty string
:   Behaves the same as **auto**.

left
:   Insert page breaks after the element until it reaches a blank left page

right
:   Insert page breaks after the element until it reaches a blank right page

inherit
:   Specifies that the value of the page-break-after property should be inherited from the parent element

## Related specifications

[CSS Fragmentation Module Level 3, 3.3. Page Break Aliases: the ‘page-break-before’, ‘page-break-after’, and ‘page-break-inside’ properties](http://www.w3.org/TR/css3-break/#page-break)
:   W3C Working Draft

[CSS Paged Media Module Level 3, 9. Page Breaks](http://www.w3.org/TR/css3-page/#page-breaks)
:   W3C Working Draft

[CSS Level 2 (Revision 1), 13.3.1 Page break properties: 'page-break-before', 'page-break-after', 'page-break-inside'](http://www.w3.org/TR/CSS2/page.html#page-break-props)
:   W3C Recommendation

