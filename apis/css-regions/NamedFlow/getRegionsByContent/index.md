---
title: getRegionsByContent()
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/css-regions/NamedFlow
    href: /apis/css-regions/NamedFlow
  return_type:
    predicate: 'Returns an object of type  '
    value: function
    href: /apis/css-regions/NamedFlow
standardization_status: 'W3C Working Draft'
summary: 'Returns the static sequence of regions that contain at least part of the supplied target content element.'
tags:
  0: API
  1: Object
  2: Methods
  4: CSS
  5: CSS-Regions
uri: apis/css-regions/NamedFlow/getRegionsByContent

---
## Summary

Returns the static sequence of regions that contain at least part of the supplied target content element.

Method of [apis/css-regions/NamedFlow](/apis/css-regions/NamedFlow)[apis/css-regions/NamedFlow](/apis/css-regions/NamedFlow)

## Syntax

``` js
var regions = flow.getRegionsByContent(element);
```

## Parameters

### element

 Data-type
:   DOM Node

## Return Value

Returns an object of type functionfunction

Returns the static sequence of regions that contain at least part of the supplied target content element. The regions are returned in document order.

## Examples

Checks if the last paragraph in a [flow](/css/concepts/named_flow) splits across more than one region

``` js
// get flow:
var flow = document.getNamedFlows().namedItem('main');
// get all top-level flow-into elements that contribute to flow:
var elements = flow.getContent();
// get last element:
var lastElement = elements[elements.length-1];
// from within last element, get last paragraph;
var lastPara = lastElement.querySelector('p:last-of-type');
// get regions in which last paragraph displays:
var regions = flow.getRegionsByContent(lastPara);
// check if last paragraph splits across regions:
if (regions.length > 1) {
    // do something?
}
```

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

-   **getRegionsByContent()**

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
