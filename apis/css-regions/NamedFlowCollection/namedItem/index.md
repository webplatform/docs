---
title: namedItem
tags:
  - API
  - Object
  - Methods
  - CSS-Regions
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Retrieve a named flow by its name'
uri: apis/css-regions/NamedFlowCollection/namedItem

---
# namedItem()

## Summary

Retrieve a named flow by its name

*Method of [apis/css-regions/NamedFlowCollection](/apis/css-regions/NamedFlowCollection)*

## Syntax

``` {.js}
var flow = flows.namedItem(name);
```

## Parameters

### name

 Data-typeÂ
:   String

 the name of the named flow

## Return Value

Returns an object of type DOM Node.

the [**NamedFlow**](/apis/css-regions/NamedFlow) object that corresponds to the specified name

## Examples

Retrieve the *main* flow from the document, in one method-chained line:

``` {.js}
var flow = document.getNamedFlows().namedItem('main');
```

## Usage

     The NamedFlowCollection object is an array snapshot of a document's named flows. This method allows you to access a specific flow directly by its name, rather than by iterating over the array.

## Related specifications

Specification
:   Status
[CSS Regions Module Level 1](http://www.w3.org/TR/2013/WD-css3-regions-20130528/)
:   W3C Working Draft 28 May 2013

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

### External resources

-   W3C editor's draft: [CSS Regions Module Level 3](http://dev.w3.org/csswg/css3-regions/)
-   Adobe Web Standards: [CSS Regions](http://html.adobe.com/webstandards/cssregions)
-   Adobe Developer's Network: [CSS3 Regions: Rich page layout with HTML and CSS3](http://www.adobe.com/devnet/html5/articles/css3-regions.html)
-   [Sample pages](http://adobe.github.com/web-platform/samples/css-regions)

