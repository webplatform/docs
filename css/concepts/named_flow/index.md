---
title: 'named flows'
notes:
  - '"Region" and "Regions" link to content almost identical to this page. Consider merging this page with the others.'
readiness: 'In Progress'
summary: 'An object that contains content diverted from one set of elements, which can then be threaded through another series of regions that display the content.'
tags:
  - Concept_Pages
  - CSS-Regions
uri: 'css/concepts/named flow'

---
## Summary

An object that contains content diverted from one set of elements, which can then be threaded through another series of regions that display the content.

 The *CSS Regions* feature allows content to flow dynamically through a series of presentational block elements, known as [*regions*](/css/concepts/region), allowing for complex magazine-style layouts.

Two CSS properties make this feature work. The [**flow-into**](/css/properties/flow-into) property diverts content into a ***named flow***. The [**flow-from**](/css/properties/flow-from) property threads that flow's content through a dynamic series of [*region*](/css/concepts/region) elements, collectively known as a [*region chain*](/css/concepts/region_chain).

The following shows a complex layout featuring a series of regions, with a named flow's content threading through regions **1** through **4**, which form a chain. A separate named flow is assigned to the single-element region chain labeled **A**:

![regions.png](/assets/thumb/3/38/regions.png/400px-regions.png)

There can be more than one **named flow** in a document. Each named flow can accumulate content from more than one element via the [**flow-into**](/css/properties/flow-into) property, but they do so according to the order in which they appear in the document. Use the [**NamedFlow**](/apis/css-regions/NamedFlow) interface to programatically access the named flow's content.

For an overview of CSS Regions, see [Using CSS Regions to flow content through a layout](/tutorials/css-regions).

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

-   **named flows**

-   [overset content](/css/concepts/overset)

-   [regions](/css/concepts/region)

-   [region chains](/css/concepts/region_chain)

-   [break-after](/css/properties/break-after)

-   [break-before](/css/properties/break-before)

-   [break-inside](/css/properties/break-inside)

-   [flow-from](/css/properties/flow-from)

-   [flow-into](/css/properties/flow-into)
