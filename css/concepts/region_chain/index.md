---
title: region chains
notes:
  - 'Almost identical content to "Region", "Regions" and "Named Flow". Consider merging.'
readiness: 'In Progress'
summary: 'A series of regions that display the contents of a named flow.'
tags:
  - Concept
  - Pages
  - CSS-Regions
uri: 'css/concepts/region chain'

---
## <span>Summary</span>

A series of regions that display the contents of a named flow.

 The *CSS Regions* feature allows content to flow dynamically through a series of presentational block elements, known as [*regions*](/css/concepts/region), allowing for complex magazine-style layouts. Each available [*named flow*](/css/concepts/named_flow), identified by content elements' [**flow-into**](/css/properties/flow-into) property, threads through a **chain** of block elements whose [**flow-from**](/css/properties/flow-from) property matches. Regardless of how each region is positioned, content threads through the **region chain** in *DOM order*, the order in which regions are declared within the HTML document.

The following shows a complex layout featuring a series of regions, with a named flow's content threading through regions **1** through **4**, which form a chain. A separate named flow is assigned to the single-element region chain labeled **A**:

![regions.png](/assets/thumb/3/38/regions.png/400px-regions.png)

A **region chain** may have either not enough or too many elements to neatly display a [named flow](/css/concepts/named_flow)'s content. The [**NamedFlow**](/apis/css-regions/NamedFlow) interface's [**overset**](/apis/css-regions/NamedFlow/overset) property allows you to programatically identify the latter [*overset*](/css/concepts/overset) case for a body of content. The [**Region**](/apis/css-regions/Region) interface's [**regionOverset**](/apis/css-regions/Region/regionOverset) property allows you to identify both cases, **empty** or **overset**, by examining regions within the chain, which are available via the named flow's [**getRegions()**](/apis/css-regions/NamedFlow/getRegions) method.

For an overview of CSS Regions, see [Using CSS Regions to flow content through a layout](/tutorials/css-regions).

## <span>Related specifications</span>

[CSS Regions Module Level 1](http://www.w3.org/TR/css3-regions/)
:   W3C Working Draft

## <span>See also</span>

### <span>Related articles</span>

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

-   **region chains**

-   [break-after](/css/properties/break-after)

-   [break-before](/css/properties/break-before)

-   [break-inside](/css/properties/break-inside)

-   [flow-from](/css/properties/flow-from)

-   [flow-into](/css/properties/flow-into)

### <span>External resources</span>

-   W3C editor's draft: [CSS Regions Module Level 3](http://dev.w3.org/csswg/css3-regions/)
-   Adobe Web Standards: [CSS Regions](http://html.adobe.com/webstandards/cssregions)
-   Adobe Developer's Network: [CSS3 Regions: Rich page layout with HTML and CSS3](http://www.adobe.com/devnet/html5/articles/css3-regions.html)
-   [Sample pages](http://adobe.github.com/web-platform/samples/css-regions)
