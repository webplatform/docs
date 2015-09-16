---
title: 'overset content'
readiness: 'Ready to Use'
summary: 'Refers to a situation in which the final region of a region chain is unable to fully display remaining content of a named flow.'
tags:
  - Concept
  - Pages
  - CSS-Regions
uri: css/concepts/overset

---
## Summary

Refers to a situation in which the final region of a region chain is unable to fully display remaining content of a named flow.

 The *CSS Regions* feature allows content to flow dynamically through a series of presentational block elements, known as [*regions*](/css/concepts/region), allowing for complex magazine-style layouts. This [*region chain*](/css/concepts/region_chain) may not have enough room to accommodate all the content. In that case, illustrated below as *Scenario \#2*, the final region is in an ***overset*** state, as is the [*named flow*](/css/concepts/named_flow) that contains all the content.

Depending on its [**region-fragment**](/css/properties/region-fragment) property, the final [region's](/css/concepts/region) content may appear as a [*fragment*](/css/concepts/fragment), breaking cleanly as if there were subsequent regions in the chain into which content could flow. Otherwise it may simply *overflow* the final element: either clipping, spilling, or scrolling past the element's dimensions as specified by the region's [**overflow**](/css/properties/overflow) property.

There are two ways to programatically detect overset state:

-   From the content side, if the [named flow's](/css/concepts/named_flow) [**overset**](/apis/css-regions/NamedFlow/overset) property is **true**, it means that it doesn't fully display within the [region chain](/css/concepts/region_chain), or that it has not been placed within any [regions](/css/concepts/region).

-   On the presentation side, if the final region element's [**regionOverset**](/apis/css-regions/Region/regionOverset) property is **overset**, some of its content can flow into another region if available.

For an overview of CSS Regions, see [Using CSS Regions to flow content through a layout](/tutorials/css-regions).

## Examples

The following example defines a set of content and a region chain into which to present it. Resulting layout scenarios are illustrated in subsequent examples:

``` html


<style>
article.content { flow-into: main;}
section.layout > div { flow-from: main; }
</style>

<!-- CONTENT -->

<article class="content">
  <p>Content #1</p>
  <p>Content #2</p>
  ...
  <p>Content #n</p>
  <p>Final Content</p>
</article>

<!-- LAYOUT -->

<section class="layout">
  <div>Region #1</div>
  <div>Region #2</div>
  <div>Region #3</div>
  <div>Region #4</div>
</section>
```

</pre>

*Scenario \#1:* If the region provides enough area, the final content element appears within the final region. The final **div** element's [**regionOverset**](/apis/css-regions/Region/regionOverset) property returns **fit**. Note that this is *not* valid DOM structure, and simply illustrates how content [*fragments*](/css/concepts/fragment) flow dynamically within the region chain.

``` html


<section class="layout">
  <div>
            <article class="content">
              <p>Content #1</p>
              <p>Content...
  </div>
  <div>
              ...#2</p>
  </div>
  <div>
              ...
              <p>Content #n</p>
  </div>
  <div>
              <p>Final Content</p>
             </article>
  </div>
</section>
```

</pre>

*Scenario \#2:* This shows the same situation, but with not enough area in the region chain to display *overset* content. The final **div** element's [**regionOverset**](/apis/css-regions/Region/regionOverset) property returns **overset**. The named flow's [**overset**](/apis/css-regions/NamedFlow/overset) property likewise returns **true**.

``` html


<section class="layout">
  <div>
            <article class="content">
              <p>Content #1</p>
              <p>Content...
  </div>
  <div>
              ...#2</p>
  </div>
  <div>
              ...
  </div>
  <div>
              <p>Content #n</p>
  </div>
</section>

<!-- OVERSET CONTENT, DOES NOT DISPLAY:
              <p>Final Content</p>
             </article>
-->
```

</pre>

*Scenario \#3:* In this example, there is *not enough* content to fill the region chain. The final **div** element's [**regionOverset**](/apis/css-regions/Region/regionOverset) property returns **empty**.

``` html


<section class="layout">
  <div>
            <article class="content">
              <p>Content #1</p>
              <p>Content...
  </div>
  <div>
              ...#2</p>
              ...
              <p>Content #n</p>
  </div>
  <div>
              <p>Final Content</p>
             </article>
  </div>
  <div>
              <!-- EMPTY REGION -->
  </div>
</section>
```

</pre>

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

-   **overset content**

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
