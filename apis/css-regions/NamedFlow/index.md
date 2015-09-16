---
title: 'NamedFlow'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Represents content to flow among various block region elements. The NamedFlow interface allows access to both the content of the flow and the series of regions in which it displays, and helps determine if the content exceeds or falls short of the number of regions necessary to display it.'
tags:
  0: API
  1: Objects
  3: CSS
  4: CSS-Regions
uri: apis/css-regions/NamedFlow

---
## Summary

Represents content to flow among various block region elements. The NamedFlow interface allows access to both the content of the flow and the series of regions in which it displays, and helps determine if the content exceeds or falls short of the number of regions necessary to display it.

## Properties

API Name
:   Summary

[firstEmptyRegionIndex](/apis/css-regions/NamedFlow/firstEmptyRegionIndex)
:   Returns the integer index of the first empty element within a [region chain](/css/concepts/region_chain). Returns -1 if the content fits within the [region chain](/css/concepts/region_chain), if it exceeds available space or if there are no regions in the [region chain](/css/concepts/region_chain).

[name](/apis/css-regions/NamedFlow/name)
:   Name of [flow](/css/concepts/named_flow), as specified by any element's [**flow-from**](/css/properties/flow-from) or [**flow-into**](/css/properties/flow-into) properties.

[overset](/apis/css-regions/NamedFlow/overset)
:   Indicates whether a [flow's](/css/concepts/named_flow) content exceeds available space within a [region chain](/css/concepts/region_chain), or if no available chain in which to flow content exists.

## Methods

API Name
:   Summary

[getContent](/apis/css-regions/NamedFlow/getContent)
:   Returns a static collection of nodes representing the [flow's](/css/concepts/named_flow) source content.

[getRegions](/apis/css-regions/NamedFlow/getRegions)
:   Returns the static sequence of [regions](/css/concepts/region) into which content flows.

[getRegionsByContent](/apis/css-regions/NamedFlow/getRegionsByContent)
:   Returns the static sequence of [regions](/css/concepts/region) that contain at least part of the supplied target content element.

## Events

API Name
:   Summary

[regionfragmentchange](/apis/css-regions/NamedFlow/regionfragmentchange)
:   Fires on the ****NamedFlow**** object when there is a change in how content flows through a [region chain](/css/concepts/region_chain).

[regionoversetchange](/apis/css-regions/NamedFlow/regionoversetchange)
:   Fires on the ****NamedFlow**** object when a change in how its content flows through a [region chain](/css/concepts/region_chain) renders any [region](/css/concepts/region) empty or [*overset*](/css/concepts/overset) (overfilled), or that reverses that state.

## Examples

Generic event handler dispatches functions to add or delete regions based on changes to how content flows through a [region chain](/css/concepts/region_chain):

``` js
document.getNamedFlows().namedItem('main').addEventListener(
    'regionoversetchange', modifyFlow
);
document.getNamedFlows().namedItem('figures').addEventListener(
    'regionoversetchange', modifyFlow
);

function modifyFlow(e) {
    var flow = e.target;
    // does content exceed available regions?
    if (flow.overset) {
        appendRegion(flow.name); // custom function
    }
    // ...or does insufficient content leave some regions empty?
    else if (flow.firstEmptyRegionIndex !== -1) {
        trimRegions(flow.name); // custom function
    }
}
```

Check if the opening paragraph splits across layout elements:

``` js
// get flow
var flow = document.getNamedFlows().namedItem('main');

// get all top-level flow-into elements that contribute to flow:
var elements = flow.getContent();

// get first element's first paragraph...
var firstPara = elements[0].querySelector('p:first-of-type');

// ...and the regions in which it appears:
var regions = flow.getRegionsByContent(firstPara);

// If the element splits across two regions, do something to modify
// the layout or the content:
if (regions.length > 1) {
    adjustLayout(regions[0], firstPara); // custom function
}
```

## Usage

     Specifying an identifier for any element's flow-into CSS property diverts its content to a NamedFlow object, whose name corresponds to the property's value.  Other elements that specify the same identifier as their flow-from property serve as a chain of 'regions' that dynamically display the content.  (The NamedFlow object is still available with NULL content if those properties are later removed.)

Use the [**getNamedFlows()**](/dom/Document/getNamedFlows) method to gather [named flows](/css/concepts/named_flow) from a document.

For an overview of CSS Regions, see [Using CSS Regions to flow content through a layout](/tutorials/css-regions).

## Related specifications

[CSS Regions Module Level 1](http://www.w3.org/TR/css3-regions/)
:   W3C Working Draft

## See also

### Related articles

#### Regions

-   [CSS Regions API](/apis/css-regions)

-   [CSSRegionStyleRule](/apis/css-regions/CSSRegionStyleRule)

-   **NamedFlow**

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
