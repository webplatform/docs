---
title: 'CSS Regions API'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Programmatic interface to content that flows through a series of chained region elements.'
tags:
  - API_Listings
  - API
  - CSS-Regions
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/css-regions/NamedFlowMap
uri: apis/css-regions

---
## Summary

Programmatic interface to content that flows through a series of chained region elements.

|Page|Summary|
|:---|:------|
|[CSSRegionStyleRule](/apis/css-regions/CSSRegionStyleRule)|Represents an [**@region**](/css/atrules/@region) rule in a CSS style sheet, which applies styles to [fragments](/css/concepts/fragment) of content that flow into a CSS [region](/css/concepts/region).|
|[NamedFlow](/apis/css-regions/NamedFlow)|Represents content to flow among various block [*region*](/css/concepts/region) elements. The **NamedFlow** interface allows access to both the content of the [flow](/css/concepts/named_flow) and the series of regions in which it displays, and helps determine if the content exceeds or falls short of the number of regions necessary to display it.|
|[NamedFlowCollection](/apis/css-regions/NamedFlowCollection)|Obsolete. Replaced by [NamedFlowMap](/w/index.php?title=apis/css-regions/NamedFlowMap&action=edit&redlink=1). Represents a static snapshot array of a document's available [named flows](/css/concepts/named_flow)|
|[Region](/apis/css-regions/Region)|The **Region** interface is available for any element that serves as a CSS [*region*](/css/concepts/region), whose [**flow-from**](/css/properties/flow-from) CSS specifies it displays content from a [named flow](/css/concepts/named_flow).|

## Usage

     CSS Regions are defined by two CSS properties.  The

[**flow-into**](/css/properties/flow-into) property diverts content into a [*named flow*](/css/concepts/named_flow), and the [**flow-from**](/css/properties/flow-from) property pours that flow's content through a dynamic [chain](/css/concepts/region_chain) of [*region*](/css/concepts/region) elements. The feature allows content to follow a path through arbitrarily placed magazine-style layout elements. Use as follows:

-   The [**getNamedFlows()**](/dom/Document/getNamedFlows) method, available via the [**Document**](/dom/Document) interface, retrieves all of a document's named flows as a [**NamedFlowCollection**](/apis/css-regions/NamedFlowCollection).

-   Iterate over the [**NamedFlowCollection**](/apis/css-regions/NamedFlowCollection) as an array, or call [**namedItem**](/apis/css-regions/NamedFlowCollection/namedItem) on it to access each [**NamedFlow**](/apis/css-regions/NamedFlow) by its name.

-   The [**NamedFlow**](/apis/css-regions/NamedFlow) interface provides access to the content defined as [**flow-into**](/css/properties/flow-into), and the series of layout regions defined as [**flow-from**](/css/properties/flow-from). Use it to check if the amount of content matches the allotted set of regions in which it appears.

-   The [**Region**](/apis/css-regions/Region) interface provides information on each region within the chain, and allows access to [fragments](/css/concepts/fragment) of content that dynamically appear there.

For an overview of CSS Regions, see [Using CSS Regions to flow content through a layout](/tutorials/css-regions).

## See also

### Related articles

#### Regions

-   **CSS Regions API**

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

-   [break-inside](/css/properties/break-inside)

-   [flow-from](/css/properties/flow-from)

-   [flow-into](/css/properties/flow-into)

### External resources

-   W3C editor's draft: [CSS Regions Module Level 3](http://dev.w3.org/csswg/css3-regions/)
-   Adobe Web Standards: [CSS Regions](http://html.adobe.com/webstandards/cssregions)
-   Adobe Developer's Network: [CSS3 Regions: Rich page layout with HTML and CSS3](http://www.adobe.com/devnet/html5/articles/css3-regions.html)
-   [Sample pages](http://adobe.github.com/web-platform/samples/css-regions)
