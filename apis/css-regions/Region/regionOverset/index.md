---
title: 'regionOverset'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/css-regions/Region
    href: /apis/css-regions/Region
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /apis/css-regions/Region
standardization_status: 'W3C Working Draft'
summary: 'A region''s display state within a region chain.'
tags:
  0: API
  1: Object
  2: Properties
  4: CSS
  5: CSS-Regions
uri: apis/css-regions/Region/regionOverset

---
## Summary

A region's display state within a region chain.

Property of [apis/css-regions/Region](/apis/css-regions/Region)[apis/css-regions/Region](/apis/css-regions/Region)

## Syntax

**Note**: This property is read-only.

``` js
var regionState = region.regionOverset;
```

## Return Value

Returns an object of type StringString

A [region's](/css/concepts/region) display state within a [region chain](/css/concepts/region_chain):

-   **overset** indicates the region is the last in the [chain](/css/concepts/region_chain), and does not have enough room to display remaining content. See [**region-fragment**](/css/properties/region-fragment) for display options.

-   **empty** indicates content was accommodated by previous regions in the [chain](/css/concepts/region_chain), or that no content is available to flow into the [chain](/css/concepts/region_chain).

-   **fit** indicates various scenarios:

-   -   When content appears within the last region in the [chain](/css/concepts/region_chain) but does not overflow it, as described above in **overset**

-   -   For regions that flow content into subsequent regions in the [chain](/css/concepts/region_chain)

-   -   For regions that are too small to display the next available item of content, such as an image, which gets pushed into a subsequent region

-   -   For elements that no longer behave as a region, which occurs when their [**flow-from**](/css/properties/flow-from) property reverts to **none**

## Examples

Check if region needs to be deleted or appended:

``` js
if (region.regionOverset == 'empty') {
    // delete region?
} else if (region.regionOverset == 'overset') {
    // add additional regions?
}
```

## Notes

Not to be confused with [**overset**](/apis/css-regions/NamedFlow/overset), which indicates whether the overall [named flow](/css/concepts/named_flow) features too few display regions.

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

-   [getRegionFlowRanges()](/apis/css-regions/Region/getRegionFlowRanges)

-   **regionOverset**

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
