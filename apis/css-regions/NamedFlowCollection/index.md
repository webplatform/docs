---
title: NamedFlowCollection
tags:
  - API
  - Objects
  - CSS-Regions
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Obsolete. Replaced by NamedFlowMap. Represents a static snapshot array of a document''s available named flows'
uri: apis/css-regions/NamedFlowCollection
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/css-regions/NamedFlowMap

---
# NamedFlowCollection

## Summary

Obsolete. Replaced by NamedFlowMap. Represents a static snapshot array of a document's available named flows

## Properties

*No properties.*

## Methods

API Name
:   Summary
[namedItem](/apis/css-regions/NamedFlowCollection/namedItem)
:   Retrieve a [named flow](/css/concepts/named_flow) by its name

## Events

*No events.*

## Examples

Retrieve the *main* flow from the document, in one method-chained line:

``` {.js}
var flow = document.getNamedFlows().namedItem('main');
```

Same as above, but iterates over the **NamedFlowCollection** object represented in a *flows* variable:

``` {.js}
var flow;
var flows = document.getNamedFlows();
for (var i = 0; i < flows.length; i++) {
    if (flows[i].name == 'main') {
        flow = flows[i];
        break;
    }
}
```

## Usage

     For any flows in the collection that  disappear when they are no longer assigned to any content, item() and namedItem() yield null.

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

-   **NamedFlowCollection**

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

