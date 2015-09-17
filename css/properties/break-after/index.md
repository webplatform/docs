---
title: 'break-after'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/7281550'
compatibility:
  feature: break-after
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'block-level elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`breakAfter`'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The CSS break-after property allows you to force a break on multi-column layouts. More specifically, it allows you to force a break after an element. It allows you to determine if a break should occur, and what type of break it should be. The break-after CSS property describes how the page, column or region break behaves after the generated box. If there is no generated box, the property is ignored.'
tags:
  - CSS_Properties
  - CSS
  - CSS-Regions
uri: css/properties/break-after

---
## Summary

The CSS break-after property allows you to force a break on multi-column layouts. More specifically, it allows you to force a break after an element. It allows you to determine if a break should occur, and what type of break it should be. The break-after CSS property describes how the page, column or region break behaves after the generated box. If there is no generated box, the property is ignored.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `auto`

Applies to
:   block-level elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `breakAfter`

## Syntax

-   `break-after: always`
-   `break-after: auto`
-   `break-after: avoid`
-   `break-after: avoid-column`
-   `break-after: avoid-page`
-   `break-after: avoid-region`
-   `break-after: column`
-   `break-after: left`
-   `break-after: page`
-   `break-after: region`
-   `break-after: right`

## Values

auto
:   Default. A page break or column break is determined by the flow of content.

always
:   A page/column/region break is inserted (forced) after the content block.

avoid
:   A page/column/region break is not allowed after the content block.

left
:   A page break is inserted (forced) after the content block, causing the flow of content to continue in the first column of the "left" page that immediately follows the current page (according to the paging format of the document).

right
:   A page break is inserted (forced) after the content block, causing the flow of content to continue in the first column of the "right" page that immediately follows the current page (according to the paging format of the document).

page
:   A page break is inserted (forced) after the content block, causing the flow of content to continue in the first column of the page that immediately follows the current page (according to the paging format of the document).

column
:   A column break is inserted (forced) after the content block.

avoid-page
:   A page break is not allowed after the content block.

avoid-column
:   A column break is not allowed after the content block.

region
:   A [region](/css/concepts/region) break is inserted (forced) after the content block.

avoid-region
:   A [region](/css/concepts/region) break is not allowed after the content block.

## Examples

``` css
/* forces top-level headings onto a new page, column, or region */
h1 {
    break-before: always;
}

/* binds subheads to subsequent content,
   without necessarily forcing a page break */
h2, h3 {
    break-after: avoid;
    break-inside: avoid;
}
```

``` css
.multicol {
background-color:lightyellow;
padding:20px;

/* CSS3 */
column-count: 3;
column-rule: 5px dotted coral;
vertical-align:text-top;
}

.multicol hr {
break-after: column;
}
```

[View live example](http://gist.github.com/7281550)

## Usage

     The break-after property is not supported for absolutely positioned elements.

This property replaces separate **column-break-after**, **page-break-after**, and **region-break-after** properties, which may still be present in some browser implementations.

## Notes

The break-after property is ignored if there is no generated box or flows defined. So most of the times, you have to define a flow of content to test the property.

Each possible break point, that is each element boundary, is under the influence of three properties, the break-after value of the previous element, the break-before value of the next element and the break-inside of the containing element.

To define if a break must be done, the following rules are applied:

If any of the three concerned values is a forced break value, that is always, left, right, page, column or region, it has precedence. If several of the concerned values is such a break, the one of the element that appears the latest in the flow is taken (that is the break-before value has precedence over the break-after value, which itself has precedence over the break-inside value).

If any of the three concerned values is an avoid break value, that is avoid, avoid-page, avoid-region, avoid-column, no such break will be applied at that point.

## Related specifications

[CSS Regions Module Level 1](http://www.w3.org/TR/css3-regions/#region-flow-break)
:   W3C Working Draft

## See also

### Related articles

#### Multi-Column

-   **break-after**

-   [break-before](/css/properties/break-before)

-   [break-inside](/css/properties/break-inside)

-   [column-count](/css/properties/column-count)

-   [column-gap](/css/properties/column-gap)

-   [column-rule](/css/properties/column-rule)

-   [column-rule-color](/css/properties/column-rule-color)

-   [column-rule-style](/css/properties/column-rule-style)

-   [column-rule-width](/css/properties/column-rule-width)

-   [column-span](/css/properties/column-span)

-   [column-width](/css/properties/column-width)

-   [content](/css/properties/content)

#### Regions

-   [CSS Regions API](/apis/css-regions)

-   [CSSRegionStyleRule](/apis/css-regions/CSSRegionStyleRule)

-   [NamedFlow](/apis/css-regions/NamedFlow)

-   [firstEmptyRegionIndex](/apis/css-regions/NamedFlow/firstEmptyRegionIndex)

-   [getContent()](/apis/css-regions/NamedFlow/getContent)

-   [getRegions()](/apis/css-regions/NamedFlow/getRegions)

-   [getRegionsByContent()](/apis/css-regions/NamedFlow/getRegionsByContent)

-   [name](/apis/css-regions/NamedFlow/name)

-   [overset](/apis/css-regions/NamedFlow/overset)

-   [regionfragmentchange](/apis/css-regions/NamedFlow/regionfragmentchange)

-   [regionoversetchange](/apis/css-regions/NamedFlow/regionoversetchange)

-   [NamedFlowCollection](/apis/css-regions/NamedFlowCollection)

-   [namedItem()](/apis/css-regions/NamedFlowCollection/namedItem)

-   [Region](/apis/css-regions/Region)

-   [getComputedRegionStyle()](/apis/css-regions/Region/getComputedRegionStyle)

-   [getRegionFlowRanges()](/apis/css-regions/Region/getRegionFlowRanges)

-   [regionOverset](/apis/css-regions/Region/regionOverset)

-   [@region](/css/atrules/@region)

-   [content fragments](/css/concepts/fragment)

-   [named flows](/css/concepts/named_flow)

-   [overset content](/css/concepts/overset)

-   [regions](/css/concepts/region)

-   [region chains](/css/concepts/region_chain)

-   **break-after**

-   [break-before](/css/properties/break-before)

-   [break-inside](/css/properties/break-inside)

-   [flow-from](/css/properties/flow-from)

-   [flow-into](/css/properties/flow-into)

### Other articles

-   [Using CSS Regions to flow content through a layout](/tutorials/css-regions)

### External resources

-   W3C editor's draft: [CSS Regions Module Level 3](http://dev.w3.org/csswg/css3-regions/)
-   Adobe Web Standards: [CSS Regions](http://html.adobe.com/webstandards/cssregions)
-   Adobe Developer's Network: [CSS3 Regions: Rich page layout with HTML and CSS3](http://www.adobe.com/devnet/html5/articles/css3-regions.html)
-   [Sample pages](http://adobe.github.com/web-platform/samples/css-regions)

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   style[style](/css/cssom/style)
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
-   table[table](/html/elements/table)
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
-   `Reference`
-   breakBefore[breakBefore](/css/properties/break-before)
-   breakInside[breakInside](/css/properties/break-inside)
