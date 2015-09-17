---
title: 'getContent()'
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
summary: 'Returns a static collection of nodes representing the flow''s source content.'
tags:
  - API_Object_Methods
  - API
  - CSS
  - CSS-Regions
uri: apis/css-regions/NamedFlow/getContent

---
## Summary

Returns a static collection of nodes representing the flow's source content.

Method of [apis/css-regions/NamedFlow](/apis/css-regions/NamedFlow)[apis/css-regions/NamedFlow](/apis/css-regions/NamedFlow)

## Syntax

``` js
var elements = flow.getContent();
```

## Return Value

Returns an object of type functionfunction

Returns a static collection of nodes representing the flow's source content.

## Examples

Get the last source element whose [**flow-into**](/css/properties/flow-into) adds it to the flow:

``` js
// get flow:
var flow = document.getNamedFlows().namedItem('main');
// get all flow-into elements:
var elements = flow.getContent();
// of these, get last element:
var lastElement = elements[elements.length-1];
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

-   **getContent()**

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
