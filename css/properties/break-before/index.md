---
title: break-before
tags:
  0: CSS
  1: Properties
  3: CSS-Regions
  4: Flexbox
  5: UI
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Control page/column/region breaks that fall above a block of content'
code_samples:
  - 'http://gist.github.com/6158525'
  - 'http://gist.github.com/6167152'
uri: css/properties/break-before

---
# break-before

## Summary

Control page/column/region breaks that fall above a block of content

## Overview table

[Initial value](/css/concepts/initial_value)
:   `auto`
Applies to
:   block-level elements
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   specified value
Animatable
:   No
[CSS Object Model Property](/css/concepts/cssom)
:   `breakBefore`
Percentages
:   n/a

## Syntax

-   `break-before: always`
-   `break-before: auto`
-   `break-before: avoid`
-   `break-before: avoid-column`
-   `break-before: avoid-page`
-   `break-before: avoid-region`
-   `break-before: column`
-   `break-before: left`
-   `break-before: page`
-   `break-before: region`
-   `break-before: right`

## Values

auto
:   Default. A page break or column break is determined by the flow of content.

always
:   A page break is inserted (forced) before the content block.

avoid
:   A page/column/region break is not allowed before the content block.

left
:   A page break is inserted (forced) before the content block such that the flow of content continues in the first column of the "left" page that immediately follows the current page (according to the paging format of the document).

right
:   A page break is inserted (forced) before the content block such that the flow of content continues in the first column of the "right" page that immediately follows the current page (according to the paging format of the document).

page
:   A page break is inserted (forced) before the content block such that the flow of content continues in the first column of the page that immediately follows the current page (according to the paging format of the document).

column
:   A column break is inserted (forced) before the content block.

avoid-page
:   A page break is not allowed before the content block.

avoid-column
:   A column break is not allowed before the content block.

region
:   A [region](/css/concepts/region) break is inserted (forced) before the content block.

avoid-region
:   A [region](/css/concepts/region) break is not allowed before the content block.

## Examples

``` {.css}
/* forces top-level headings onto a new page, column, or region */
h1 {
    break-before: always;
}

/* binds subheads to subsequent content,
    without necessarily forcing a page break */
h2, h3 {
    break-after: avoid;
    break-inside: avoid;
}
```

Forces h3s onto a new column.

``` {.css}
h3 {
    break-before: always;
}
```

[View live example](http://code.webplatform.org/gist/6158525)

Currently, must use WebKit Nightly or Chrome Canary with experimental features enabled.

Assuming the main content is at div class="main" and contains h3s, and 6 div class="region", the content will flow into these 6 regions.

``` {.css}
.region {
    flow-from: main;
}

.main {
    flow-into: main;
}

/* forces h3s into a new region */
h3 {
    break-before: always;
}
```

[View live example](http://code.webplatform.org/gist/6167152)

## Usage

     This property replaces separate column-break-before, page-break-before, and region-break-before properties, which may still be present in some browser implementations.

Frequent use case is in a print stylesheet.

## Related specifications

Specification
:   Status
[CSS Regions Module Level 1](http://dev.w3.org/csswg/css3-regions/)
:   W3C Working Draft
[CSS Fragmentation Module Level 3](http://www.w3.org/TR/css3-break/#break-properties)
:   W3C Working Draft
[CSS Multi-column Layout Module](http://www.w3.org/TR/css3-multicol/#column-breaks)
:   W3C Candidate Recommendation

## See also

### Related articles

#### CSS Layout

-   [Responsive Web Design](/concepts/mobile_web/responsive_design)

-   [@import](/css/atrules/@import)

-   [align-self](/css/properties/align-self)

-   [background](/css/properties/background)

-   [box-decoration-break](/css/properties/box-decoration-break)

-   [box-flex](/css/properties/box-flex)

-   [box-lines](/css/properties/box-lines)

-   [box-ordinal-group](/css/properties/box-ordinal-group)

-   [box-orient](/css/properties/box-orient)

-   [box-pack](/css/properties/box-pack)

-   [box-shadow](/css/properties/box-shadow)

-   **break-before**

-   [flex-align](/css/properties/flex-align)

-   [flex-item-align](/css/properties/flex-item-align)

-   [flex-line-pack](/css/properties/flex-line-pack)

-   [grid-auto-rows](/css/properties/grid-auto-rows)

-   [grid-definition-columns](/css/properties/grid-definition-columns)

-   [grid-definition-rows](/css/properties/grid-definition-rows)

-   [height](/css/properties/height)

-   [max-width](/css/properties/max-width)

-   [user-modify](/css/properties/user-modify)

-   [baseline-shift](/svg/attributes/baseline-shift)

#### Box Model

-   [border](/css/properties/border)

-   [border-corner-shape](/css/properties/border-corner-shape)

-   [bottom](/css/properties/bottom)

-   [box-shadow](/css/properties/box-shadow)

-   [box-sizing](/css/properties/box-sizing)

-   **break-before**

-   [clear](/css/properties/clear)

-   [float](/css/properties/float)

-   [height](/css/properties/height)

-   [left](/css/properties/left)

-   [line-height](/css/properties/line-height)

-   [margin](/css/properties/margin)

-   [margin-bottom](/css/properties/margin-bottom)

-   [margin-left](/css/properties/margin-left)

-   [margin-right](/css/properties/margin-right)

-   [margin-top](/css/properties/margin-top)

-   [max-height](/css/properties/max-height)

-   [max-width](/css/properties/max-width)

-   [min-height](/css/properties/min-height)

-   [min-width](/css/properties/min-width)

#### CSS Attributes

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [background-position](/css/properties/background-position)

-   **break-before**

-   [height](/css/properties/height)

-   [list-style](/css/properties/list-style)

-   [list-style-position](/css/properties/list-style-position)

-   [text-overflow-ellipsis](/css/properties/text-overflow-ellipsis)

-   [text-overflow-mode](/css/properties/text-overflow-mode)

-   [text-rendering](/css/properties/text-rendering)

-   [user-select](/css/properties/user-select)

-   [equality](/css/selectors/attributes/equality)

-   [Attribute selector](/css/selectors/attributes/existence)

-   [hyphen](/css/selectors/attributes/hyphen)

-   [prefix](/css/selectors/attributes/prefix)

-   [substring](/css/selectors/attributes/substring)

-   [suffix](/css/selectors/attributes/suffix)

-   [baseline-shift](/svg/attributes/baseline-shift)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

#### Flexbox

-   [align-content](/css/properties/align-content)

-   [align-items](/css/properties/align-items)

-   [align-self](/css/properties/align-self)

-   **break-before**

-   [flex](/css/properties/flex)

-   [flex-basis](/css/properties/flex-basis)

-   [flex-direction](/css/properties/flex-direction)

-   [flex-flow](/css/properties/flex-flow)

-   [flex-grow](/css/properties/flex-grow)

-   [flex-shrink](/css/properties/flex-shrink)

-   [flex-wrap](/css/properties/flex-wrap)

-   [justify-content](/css/properties/justify-content)

#### Multi-Column

-   [break-after](/css/properties/break-after)

-   **break-before**

-   [break-inside](/css/properties/break-inside)

-   [column-count](/css/properties/column-count)

-   [column-gap](/css/properties/column-gap)

-   [column-rule](/css/properties/column-rule)

-   [column-rule-color](/css/properties/column-rule-color)

-   [column-rule-style](/css/properties/column-rule-style)

-   [column-rule-width](/css/properties/column-rule-width)

-   [column-span](/css/properties/column-span)

-   [column-width](/css/properties/column-width)

-   [content](/css/properties/content)

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

-   [content fragments](/css/concepts/fragment)

-   [named flows](/css/concepts/named_flow)

-   [overset content](/css/concepts/overset)

-   [regions](/css/concepts/region)

-   [region chains](/css/concepts/region_chain)

-   [break-after](/css/properties/break-after)

-   **break-before**

-   [break-inside](/css/properties/break-inside)

-   [flow-from](/css/properties/flow-from)

-   [flow-into](/css/properties/flow-into)

#### Responsive Web Design

-   **break-before**

-   [column-count](/css/properties/column-count)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

#### Shapes

-   **break-before**

### External resources

-   Adobe Web Standards: [CSS Regions](http://html.adobe.com/webstandards/cssregions)
-   Adobe Developer's Network: [CSS3 Regions: Rich page layout with HTML and CSS3](http://www.adobe.com/devnet/html5/articles/css3-regions.html)
-   [Sample pages](http://adobe.github.com/web-platform/samples/css-regions)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

