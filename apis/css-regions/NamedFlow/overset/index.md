---
title: overset
tags:
  0: API
  1: Object
  2: Properties
  4: CSS
  5: CSS-Regions
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Indicates whether a flow''s content exceeds available space within a region chain, or if no available chain in which to flow content exists.'
uri: apis/css-regions/NamedFlow/overset

---
# overset

## Summary

Indicates whether a flow's content exceeds available space within a region chain, or if no available chain in which to flow content exists.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/css-regions/NamedFlow](/apis/css-regions/NamedFlow)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var exceedsRegions = flow.overset;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

Indicates whether a flow's content exceeds available space within a [region chain](/css/concepts/region_chain). Also indicates when no chain is available in which to flow content.

## Examples

``` {.js}
// adds a region element to a prescribed container
// if there aren't already enough to display all content
function appendRegion(flowName) {
    var flow = document.getNamedFlows().namedItem(flowName);
    var layout = document.querySelector('#layout_wrapper');
    var region;

    // need to add more regions?
    if (! flow.overset) return(false);

    // assumes CSS such as:
    //   #layout_wrapper > div { flow-from: mainFlow}
    region = document.createElement('div');
    layout.appendChild(region);

    return(true); // perhaps for use in while loop
}

appendRegion('mainFlow');
```

## Notes

Not to be confused with [**regionOverset**](/apis/css-regions/Region/regionOverset), which indicates the [overset](/css/concepts/overset) state of individual [regions](/css/concepts/region). Only the final region in a [chain](/css/concepts/region_chain) can be overset.

## Related specifications

Specification
:   Status
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

-   **overset**

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

