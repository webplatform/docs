---
title: page-break-before
tags:
  - CSS
  - Properties
readiness: 'Not Ready'
standardization_status: Deprecated
notes:
  - 'Deprecated; deletion candidate'
summary: 'The page-break-before property sets the page-breaking behavior before an element. With CSS3, page-break-* properties are only aliases of the break-* properties. The CSS3 Fragmentation spec defines breaks for all CSS box fragmentation.'
uri: css/properties/page-break-before

---
# page-break-before

## Summary

The page-break-before property sets the page-breaking behavior before an element. With CSS3, page-break-\* properties are only aliases of the break-\* properties. The CSS3 Fragmentation spec defines breaks for all CSS box fragmentation.

## Overview table

[Initial value](/css/concepts/initial_value)
:   ``
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
:   ``

## Syntax

-   `page-break-before: always`
-   `page-break-before: auto`
-   `page-break-before: avoid`
-   `page-break-before: empty string`
-   `page-break-before: inherit`
-   `page-break-before: left`
-   `page-break-before: right`

## Values

auto
:   Default. Insert a page break before the element if necessary.

always
:   Insert a page break before the element.

avoid
:   Avoid inserting a page break before the element.

empty string
:   Behaves the same as **auto**.

left
:   Insert page breaks before the element until it reaches a blank left page.

right
:   Insert page breaks before the element until it reaches a blank right page.

inherit
:   Specifies that the value of the page-break-before property should be inherited from the parent element

## Related specifications

Specification
:   Status
[CSS Fragmentation Module Level 3, 3.3. Page Break Aliases: the ‘page-break-before’, ‘page-break-after’, and ‘page-break-inside’ properties](http://www.w3.org/TR/css3-break/#page-break)
:   W3C Working Draft
[CSS Paged Media Module Level 3, 9. Page Breaks](http://www.w3.org/TR/css3-page/#page-breaks)
:   W3C Working Draft
[CSS Level 2 (Revision 1), 13.3.1 Page break properties: 'page-break-before', 'page-break-after', 'page-break-inside'](http://www.w3.org/TR/CSS2/page.html#page-break-props)
:   W3C Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

