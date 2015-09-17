---
title: 'flow-from'
code_samples:
  - 'http://codepen.io/collection/jabto'
compatibility:
  feature: flow-from
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'Non-replaced block containers. (May expand in the future to include other containers.)'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`flowFrom`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Flows content from a named flow (specified by a corresponding flow-into) through selected elements to form a dynamic chain of layout regions.'
tags:
  - CSS_Properties
  - CSS
  - CSS-Regions
uri: css/properties/flow-from

---
## Summary

Flows content from a named flow (specified by a corresponding flow-into) through selected elements to form a dynamic chain of layout regions.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `none`

Applies to
:   Non-replaced block containers. (May expand in the future to include other containers.)

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `flowFrom`

Percentages
:   N/A

## Syntax

-   `flow-from: <ident>`
-   `flow-from: none`

## Values

\<ident\>
:   Identifier that replaces content from specified named flow, flowing it from one [*region*](/css/concepts/region) element to another.

none
:   This container is not a region. Keeps element as is, and does not transform it into a region and replace its content.

## Examples

The following CSS...

``` css
article.content {
    flow-into: main;
}

section.layout > div {
    flow-from: main;
}
```

...flows the article through the series of **div** elements, transforming them into [*regions*](/css/concepts/region) and replacing the placeholder text:

``` html


<!-- CONTENT -->

<article class="content">
  ...
</article>

<!-- LAYOUT -->

<section class="layout">
  <div>Region #1</div>
  <div>Region #2</div>
  <div>Region #3</div>
  <div>Region #4</div>
  <div>Region #5</div>
</section>
```

</pre>

## Usage

     While regions can be positioned arbitrarily on the screen, their order in the document determines the order in which content flows. Regions otherwise do not have to appear as a continuous series within the DOM.

Descendants of any element whose ****flow-from**** specifies a named flow are suppressed from display, making their own ****flow-from**** values irrelevant.

For an overview of CSS Regions, see [Using CSS Regions to flow content through a layout](/tutorials/css-regions).

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

-   **flow-from**

-   [flow-into](/css/properties/flow-into)

### External resources

-   W3C editor's draft: [CSS Regions Module Level 3](http://dev.w3.org/csswg/css3-regions/)
-   Adobe Web Standards: [CSS Regions](http://html.adobe.com/webstandards/cssregions)
-   Adobe Developer's Network: [CSS3 Regions: Rich page layout with HTML and CSS3](http://www.adobe.com/devnet/html5/articles/css3-regions.html)
-   [Sample pages](http://adobe.github.com/web-platform/samples/css-regions)
-   [Additional examples on codpen.io](http://codepen.io/collection/jabto). This experimental feature is in WebKit (Chrome and Safari) and Trident (Internet Explorer). Enable experimental features to see how CSS Regions works.
