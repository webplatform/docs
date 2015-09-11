---
title: namedItem()
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/css-regions/NamedFlowCollection
    href: /apis/css-regions/NamedFlowCollection
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/css-regions/NamedFlowCollection
standardization_status: 'W3C Working Draft'
summary: 'Retrieve a named flow by its name'
tags:
  - API
  - Object
  - Methods
  - CSS-Regions
uri: apis/css-regions/NamedFlowCollection/namedItem

---
## <span>Summary</span>

Retrieve a named flow by its name

Method of [apis/css-regions/NamedFlowCollection](/apis/css-regions/NamedFlowCollection)[apis/css-regions/NamedFlowCollection](/apis/css-regions/NamedFlowCollection)

## <span>Syntax</span>

``` js
var flow = flows.namedItem(name);
```

## <span>Parameters</span>

### <span>name</span>

 Data-type
:   String

 the name of the named flow

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

the [**NamedFlow**](/apis/css-regions/NamedFlow) object that corresponds to the specified name

## <span>Examples</span>

Retrieve the *main* flow from the document, in one method-chained line:

``` js
var flow = document.getNamedFlows().namedItem('main');
```

## <span>Usage</span>

     The NamedFlowCollection object is an array snapshot of a document's named flows. This method allows you to access a specific flow directly by its name, rather than by iterating over the array.

## <span>Related specifications</span>

[CSS Regions Module Level 1](http://www.w3.org/TR/2013/WD-css3-regions-20130528/)
:   W3C Working Draft 28 May 2013

## <span>See also</span>

### <span>Related articles</span>

#### <span>Regions</span>

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

-   **namedItem()**

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

### <span>External resources</span>

-   W3C editor's draft: [CSS Regions Module Level 3](http://dev.w3.org/csswg/css3-regions/)
-   Adobe Web Standards: [CSS Regions](http://html.adobe.com/webstandards/cssregions)
-   Adobe Developer's Network: [CSS3 Regions: Rich page layout with HTML and CSS3](http://www.adobe.com/devnet/html5/articles/css3-regions.html)
-   [Sample pages](http://adobe.github.com/web-platform/samples/css-regions)
