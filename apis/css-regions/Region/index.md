---
title: 'Region'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The Region interface is available for any element that serves as a CSS region, whose flow-from CSS specifies it displays content from a named flow.'
tags:
  - API_Objects
  - API
  - CSS-Regions
uri: apis/css-regions/Region

---
## Summary

The Region interface is available for any element that serves as a CSS region, whose flow-from CSS specifies it displays content from a named flow.

## Properties

[regionOverset](/apis/css-regions/Region/regionOverset)
:   A [region's](/css/concepts/region) display state within a [region chain](/css/concepts/region_chain).

## Methods

[getComputedRegionStyle](/apis/css-regions/Region/getComputedRegionStyle)
:   Returns styles calculated for an element as it appears within a [region](/css/concepts/region), including styles from [**@region**](/css/atrules/@region) rules applied to ranges within the element.

[getRegionFlowRanges](/apis/css-regions/Region/getRegionFlowRanges)
:   Returns a series of [**Range**](/dom/Range) objects that represent the [fragments](/css/concepts/fragment) of DOM content that currently flow into the [region](/css/concepts/region).

## Events

*No events.*

## Examples

Determines if an element is currently set to behave as a region:

``` js
function isRegion(node) {
    // element never behaved as a region:
    if (! node.getRegionFlowRanges) return(false);
    // element only previously behaved as a region:
    if (node.getRegionFlowRanges() == null) return(false);
    // element is currently a region:
    return(true);
}
```

## Usage

     Use the Region interface to determine whether any content flows through the region, what content currently displays, and any special CSS styling that applies.

The interface is still available for elements that change back to non-region elements, when their [**flow-from**](/css/properties/flow-from) property becomes **none**.

## Notes

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

-   **Region**

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
