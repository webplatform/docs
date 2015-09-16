---
title: 'name'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/css-regions/NamedFlow
    href: /apis/css-regions/NamedFlow
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /apis/css-regions/NamedFlow
standardization_status: 'W3C Working Draft'
summary: 'Name of flow, as specified by any element''s  flow-from or flow-into properties.'
tags:
  0: API
  1: Object
  2: Properties
  4: CSS
  5: CSS-Regions
uri: apis/css-regions/NamedFlow/name

---
## Summary

Name of flow, as specified by any element's flow-from or flow-into properties.

Property of [apis/css-regions/NamedFlow](/apis/css-regions/NamedFlow)[apis/css-regions/NamedFlow](/apis/css-regions/NamedFlow)

## Syntax

**Note**: This property is read-only.

``` js
var id = flow.name;
```

## Return Value

Returns an object of type StringString

Name of flow, as specified by any element's [**flow-from**](/css/properties/flow-from) or [**flow-into**](/css/properties/flow-into) properties.

## Examples

``` js
// Generic event handler adds/deletes regions to fit content. The 'name'
// property might allow the handler to dispatch different functions for
// different flows.

function modifyFlow(e) {
    var flow = e.target;
    if (flow.overset) {
        appendRegion(flow.name);
    }
    else if (flow.firstEmptyRegionIndex !== -1) {
        trimRegions(flow.name);
    }
}

document.getNamedFlows().namedItem('main').addEventListener('regionoversetchange', modifyFlow);
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

-   [getRegionsByContent()](/apis/css-regions/NamedFlow/getRegionsByContent)

-   **name**

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
