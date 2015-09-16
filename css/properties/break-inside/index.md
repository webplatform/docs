---
title: break-inside
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Complete specifications, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'block-level elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`breakInside`'
readiness: 'In Progress'
summary: 'Control page/column/region breaks that fall within a block of content'
tags:
  0: CSS
  1: Properties
  3: CSS-Regions
uri: css/properties/break-inside

---
## Summary

Control page/column/region breaks that fall within a block of content

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
:   `breakInside`

## Syntax

-   `break-inside: auto`
-   `break-inside: avoid`
-   `break-inside: avoid-column`
-   `break-inside: avoid-page`
-   `break-inside: avoid-region`

## Values

auto
:   Default. A page/column/region break is determined by the flow of content.

avoid
:   A page/column/region break is not allowed within the content block.

avoid-page
:   A page break is not allowed within the content block.

avoid-column
:   A column break is not allowed within the content block.

avoid-region
:   A [region](/css/concepts/region) break is not allowed within the content block.

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

## Usage

     This property replaces separate column-break-inside, page-break-inside, and region-break-inside properties, which may still be present in some browser implementations.

## Related specifications

[CSS Regions Module Level 1](http://dev.w3.org/csswg/css3-regions/)
:

## See also

### Related articles

#### Multi-Column

-   [break-after](/css/properties/break-after)

-   [break-before](/css/properties/break-before)

-   **break-inside**

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

-   [break-after](/css/properties/break-after)

-   [break-before](/css/properties/break-before)

-   **break-inside**

-   [flow-from](/css/properties/flow-from)

-   [flow-into](/css/properties/flow-into)

### External resources

-   W3C editor's draft: [CSS Regions Module Level 3](http://dev.w3.org/csswg/css3-regions/)
-   Adobe Web Standards: [CSS Regions](http://html.adobe.com/webstandards/cssregions)
-   Adobe Developer's Network: [CSS3 Regions: Rich page layout with HTML and CSS3](http://www.adobe.com/devnet/html5/articles/css3-regions.html)
-   [Sample pages](http://adobe.github.com/web-platform/samples/css-regions)

### Related pages

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `style`
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
-   `Reference`
-   `breakAfter`
-   `breakBefore`
