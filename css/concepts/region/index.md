---
title: regions
readiness: 'Ready to Use'
summary: 'The CSS Regions feature allows content to flow dynamically through a series of presentational block elements, known as regions, allowing for complex magazine-style layouts.'
tags:
  - Concept
  - Pages
  - CSS-Regions
uri: css/concepts/region

---
## Summary

The CSS Regions feature allows content to flow dynamically through a series of presentational block elements, known as regions, allowing for complex magazine-style layouts.

 Two CSS properties make it work. The [**flow-into**](/css/properties/flow-into) property diverts content into a [*named flow*](/css/concepts/named_flow). The corresponding [**flow-from**](/css/properties/flow-from) property threads that flow's content through a dynamic series of ***region*** elements, collectively known as a [*region chain*](/css/concepts/region_chain). The feature allows content to thread through a document's regions, magazine-style. Regions can be positioned using various other CSS techniques, such as [flexible boxes](/tutorials/flexbox), [fixed positioning](/tutorials/CSS_absolute_and_fixed_positioning), [floats](/tutorials/floats_and_clearing), or grids.

The following shows a complex layout featuring a series of regions, with a named flow's content threading through regions **1** through **4**, which form a chain. A separate named flow is assigned to the region labeled **A**:

![regions.png](/assets/thumb/3/38/regions.png/400px-regions.png)

Assigning [**flow-from**](/css/properties/flow-from) to a block element turns it into a region. As long as it serves as a region, any of its nested content is obscured by content diverted from other elements whose [**flow-into**](/css/properties/flow-into) property specifies the same [*named flow*](/css/concepts/named_flow). If there is no corresponding [**flow-into**](/css/properties/flow-into) content, the region displays empty content.

Use the [region API's](/apis/css-regions) [**Region**](/apis/css-regions/Region) interface to programatically access each region within a chain, and the [**NamedFlow**](/apis/css-regions/NamedFlow) interface to access the overall content that flows within the chain.

For an overview of CSS Regions, see [Using CSS Regions to flow content through a layout](/tutorials/css-regions).

## Related specifications

[CSS Regions Module Level 1](http://www.w3.org/TR/css3-regions/)
:   W3C Working Draft

## See also

### Related articles

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

-   **regions**

-   [region chains](/css/concepts/region_chain)

-   [break-after](/css/properties/break-after)

-   [break-before](/css/properties/break-before)

-   [break-inside](/css/properties/break-inside)

-   [flow-from](/css/properties/flow-from)

-   [flow-into](/css/properties/flow-into)

### External resources

-   W3C editor's draft: [CSS Regions Module Level 3](http://dev.w3.org/csswg/css3-regions/)
-   Adobe Web Standards: [CSS Regions](http://html.adobe.com/webstandards/cssregions)
-   Adobe Developer's Network: [CSS3 Regions: Rich page layout with HTML and CSS3](http://www.adobe.com/devnet/html5/articles/css3-regions.html)
-   [Sample pages](http://adobe.github.com/web-platform/samples/css-regions)
