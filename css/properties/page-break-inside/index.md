---
title: 'page-break-inside'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: page-break-inside
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
summary: 'Sets the page-breaking behavior inside an element. With CSS3, page-break-* properties are only aliases of the break-* properties. The CSS3 Fragmentation spec defines breaks for all CSS box fragmentation.'
tags:
  - CSS
  - Properties
uri: css/properties/page-break-inside

---
## Summary

Sets the page-breaking behavior inside an element. With CSS3, page-break-\* properties are only aliases of the break-\* properties. The CSS3 Fragmentation spec defines breaks for all CSS box fragmentation.

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

-   `page-break-inside: auto`
-   `page-break-inside: avoid`
-   `page-break-inside: empty string`
-   `page-break-inside: inherit`

## Values

auto
:   Default.

Neither force nor forbid a page break inside the object.

avoid
:   Forbid a page break inside the object, if possible.

empty string
:   Behaves the same as **auto**.

inherit
:   Inherit the value of the same property for the object's parent.

## Related specifications

[CSS Fragmentation Module Level 3, 3.3. Page Break Aliases: the ‘page-break-before’, ‘page-break-after’, and ‘page-break-inside’ properties](http://www.w3.org/TR/css3-break/#page-break)
:   W3C Working Draft

[CSS Paged Media Module Level 3, 9. Page Breaks](http://www.w3.org/TR/css3-page/#page-breaks)
:   W3C Working Draft

[CSS Level 2 (Revision 1), 13.3.1 Page break properties: 'page-break-before', 'page-break-after', 'page-break-inside'](http://www.w3.org/TR/CSS2/page.html#page-break-props)
:   W3C Recommendation

## See also

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
-   `CSS How-to - Optimize Pages for Printing Using CSS`
