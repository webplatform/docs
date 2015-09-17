---
title: 'getRegionFlowRanges()'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/css-regions/Region
    href: /apis/css-regions/Region
  return_type:
    predicate: 'Returns an object of type  '
    value: Array
    href: /apis/css-regions/Region
standardization_status: 'W3C Working Draft'
summary: 'Returns a series of Range objects that represent the fragments of DOM content that currently flow into the region.'
tags:
  - API_Object_Methods
  - API
  - CSS
  - CSS-Regions
uri: apis/css-regions/Region/getRegionFlowRanges

---
## Summary

Returns a series of Range objects that represent the fragments of DOM content that currently flow into the region.

Method of [apis/css-regions/Region](/apis/css-regions/Region)[apis/css-regions/Region](/apis/css-regions/Region)

## Syntax

``` js
var ranges = region.getRegionFlowRanges();
```

## Return Value

Returns an object of type ArrayArray

Returns a series of [**Range**](/dom/Range) objects that represent the [fragments](/css/concepts/fragment) of DOM content that currently flow into the region.

## Examples

Check a region for interruptions in source content:

``` js
// get flow
var flow = document.getNamedFlows().namedItem('main');

// get second region that displays content
var region = flow.getRegions()[1];

// how many content fragments display there?
var ranges = region.getRegionFlowRanges();

// perhaps do something to fix layout if content has been interrupted:
if (ranges.length > 1) {
    adjustlayout(region) // custom function
}
```

## Usage

     By default, calling getRegionFlowRanges() on an overflowing region at the end of a chain (one whose regionOverset is overset) returns fragments representing all remaining content that may overflow out of view.  If the region's region-fragment property is set to break, it returns only those fragments of content that fit neatly within the region.

If the region is too small to display the content, it returns a single collapsed range.

Calling it on an empty region (one whose [**regionOverset**](/apis/css-regions/Region/regionOverset) is **empty**) returns an empty list.

Calling it on an element that is no longer a region (when its [**flow-from**](/css/properties/flow-from) property reverts to **none**) returns **null**. The following tests whether the block element currently behaves as a region:

    isRegion = (element.getRegionFlowRanges() !== null);

## Notes

Regions may display more than one range, because more than one element may specify [**flow-into**](/css/properties/flow-into) to contribute to a [flow](/css/concepts/named_flow), and the boundary between those content elements may fall within a region. Also, any content element's nested elements can be diverted to a different [named flow](/css/concepts/named_flow), thus interrupting the original sequence of content. (See [**flow-into**](/css/properties/flow-into) for more details on these scenarios.)

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

-   **getRegionFlowRanges()**

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
