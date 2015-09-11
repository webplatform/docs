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
## <span>Summary</span>

Control page/column/region breaks that fall within a block of content

## <span>Overview table</span>

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

## <span>Syntax</span>

-   `break-inside: auto`
-   `break-inside: avoid`
-   `break-inside: avoid-column`
-   `break-inside: avoid-page`
-   `break-inside: avoid-region`

## <span>Values</span>

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

## <span>Examples</span>

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

## <span>Usage</span>

     This property replaces separate column-break-inside, page-break-inside, and region-break-inside properties, which may still be present in some browser implementations.

## <span>Related specifications</span>

[CSS Regions Module Level 1](http://dev.w3.org/csswg/css3-regions/)
:

## <span>See also</span>

### <span>Related articles</span>

#### <span>Multi-Column</span>

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

#### <span>Regions</span>

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

### <span>External resources</span>

-   W3C editor's draft: [CSS Regions Module Level 3](http://dev.w3.org/csswg/css3-regions/)
-   Adobe Web Standards: [CSS Regions](http://html.adobe.com/webstandards/cssregions)
-   Adobe Developer's Network: [CSS3 Regions: Rich page layout with HTML and CSS3](http://www.adobe.com/devnet/html5/articles/css3-regions.html)
-   [Sample pages](http://adobe.github.com/web-platform/samples/css-regions)

### <span>Related pages (MSDN)</span>

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
