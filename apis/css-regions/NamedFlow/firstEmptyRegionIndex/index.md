---
title: firstEmptyRegionIndex
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/css-regions/NamedFlow
    href: /apis/css-regions/NamedFlow
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /apis/css-regions/NamedFlow
standardization_status: 'W3C Working Draft'
summary: 'Returns the integer index of the first empty element within a region chain. Returns -1 if the content fits within the region chain, if it exceeds available space or if there are no regions in the region chain.'
tags:
  0: API
  1: Object
  2: Properties
  4: CSS
  5: CSS-Regions
uri: apis/css-regions/NamedFlow/firstEmptyRegionIndex

---
## Summary

Returns the integer index of the first empty element within a region chain. Returns -1 if the content fits within the region chain, if it exceeds available space or if there are no regions in the region chain.

Property of [apis/css-regions/NamedFlow](/apis/css-regions/NamedFlow)[apis/css-regions/NamedFlow](/apis/css-regions/NamedFlow)

## Syntax

**Note**: This property is read-only.

``` js
var index = flow.firstEmptyRegionIndex;
```

## Return Value

Returns an object of type NumberNumber

Returns the integer index of the first empty element within a [region chain](/css/concepts/region_chain). Returns -1 if the content fits within the [region chain](/css/concepts/region_chain), if it exceeds available space or if there are no regions in the [region chain](/css/concepts/region_chain).

## Examples

``` js
trimRegions('mainFlow');

// deletes any empty regions from the end of a flow:
function trimRegions(flowName) {
    var flow = document.getNamedFlows().namedItem(flowName);
    var index = flow.firstEmptyRegionIndex;
    var regions = flow.getRegions();
    if (index == -1) return(false); // no empty regions?
    // remove first empty region &amp; all thereafter:
    for (var i = index; i &lt; regions.length; i++) {
        regions[i].parentNode.removeChild(regions[i]);
    }
    return(true);
}
```

## Usage

     The firstEmptyRegionIndex is the index of the first

[region](/css/concepts/region) within the [flow's](/css/concepts/named_flow) [**getRegions()**](/apis/css-regions/NamedFlow/getRegions) collection whose [**regionOverset**](/apis/css-regions/Region/regionOverset) is **empty**. If all are set to **fit** or **overset**, or if no regions are associated with the flow, the **firstEmptyRegionIndex** returns -1.

## Related specifications

[CSS Regions Module Level 1](http://www.w3.org/TR/css3-regions/)
:   W3C Working Draft

## See also

### Related articles

#### Regions

-   [CSS Regions API](/apis/css-regions)

-   [CSSRegionStyleRule](/apis/css-regions/CSSRegionStyleRule)

-   [NamedFlow](/apis/css-regions/NamedFlow)

-   **firstEmptyRegionIndex**

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
