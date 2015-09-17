---
title: 'content fragments'
notes:
  - 'Fix or remove broken link to DOM API;'
readiness: 'Almost Ready'
summary: 'A contiguous range of content, which may stretch arbitrarily across DOM nodes.'
tags:
  - Concept_Pages
  - CSS-Regions
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/traversal/Range
uri: css/concepts/fragment

---
## Summary

A contiguous range of content, which may stretch arbitrarily across DOM nodes.

 A *range* (or *fragment*) is a contiguous stretch of content within a document, one that may traverse DOM nodes arbitrarily. For example, a user may select a stretch of text that starts in the middle of one paragraph, and ends in the middle of another. CSS styling may apply dynamically to the [**::first-line**](/css/selectors/pseudo-elements/::first-line) or [**::first-letter**](/css/selectors/pseudo-elements/::first-letter) of text. Or a [*flow*](/css/concepts/named_flow) of text may thread through a series of [*region*](/css/concepts/region) elements, each of which may display only a portion of a paragraph that spills over from adjacent regions within the [chain](/css/concepts/region_chain).

You can use the [DOM Range API](/w/index.php?title=dom/traversal/Range&action=edit&redlink=1) to programatically access such arbitrary stretches of content.

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

-   [regionOverset](/apis/css-regions/Region/regionOverset)

-   [@region](/css/atrules/@region)

-   **content fragments**

-   [named flows](/css/concepts/named_flow)

-   [overset content](/css/concepts/overset)

-   [regions](/css/concepts/region)

-   [region chains](/css/concepts/region_chain)

-   [break-after](/css/properties/break-after)

-   [break-before](/css/properties/break-before)

-   [break-inside](/css/properties/break-inside)

-   [flow-from](/css/properties/flow-from)

-   [flow-into](/css/properties/flow-into)
