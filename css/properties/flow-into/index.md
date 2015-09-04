---
title: flow-into
tags:
  0: CSS
  1: Properties
  3: CSS-Regions
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Diverts the selected element''s content into a named flow, used to thread content through different layout regions specified by  flow-from.'
uri: css/properties/flow-into

---
# flow-into

## Summary

Diverts the selected element's content into a named flow, used to thread content through different layout regions specified by flow-from.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `none`
Applies to
:   Block elements, excluding pseudo-elements such as **::before** or **::after**.
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   as specified
Animatable
:   No
[CSS Object Model Property](/css/concepts/cssom)
:   `flowInto`
Percentages
:   N/A

## Syntax

-   `flow-into: <ident>`
-   `flow-into: none`

## Values

none
:   The element's content remains unchanged, and is not diverted to a flow unless an ancestor element specifies it.

\<ident\>
:   String identifier that specifies a *named flow* into which to divert the element's content. Common keyword values such as **none**, **inherit**, **default**, **auto**, and **initial** are invalid flow names, as are **element** and **content**:

-   **\<ident\> element**: The **element** keyword explicitly specifies the entire element diverts to the named flow, not just its contents. (This is the default behavior without the keyword.)

-   **\<ident\> content**: Adding the **content** keyword overrides the default behavior described above, diverting only the element's nested content to the named flow.

## Examples

The following CSS...

``` {.css}
article.content {
    flow-into: main;
}

section.layout > div {
    flow-from: main;
}
```

...flows the article through the series of **div** elements, transforming them into [*regions*](/css/concepts/region) and replacing the placeholder text:

``` {.html}


<!-- CONTENT -->

<article class="content">
  <p>Content #1</p>
  <p>Content #2</p>
  ...
  <p>Content #n</p>
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

By default, or with the **element** keyword, content appears as if structured as follows, but dynamically [*fragmenting*](/css/concepts/fragment) from one layout region to another. (Note that as presented, this is not a valid DOM structure, and simply helps to visualize how content appears in output.)

``` {.html}


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
             </article>
  </div>
</section>
```

</pre>

With the **content** keyword specified, content fragments appear as if structured as follows, *without* the interim **article** element that serves as their container:

``` {.html}


<section class="layout">
  <div>
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
```

</pre>

## Usage

     The flow-into property diverts content from where it would ordinarily appear in the document to a named flow.  It reappears elsewhere flowing through a series of region elements whose flow-from specifies the same named flow.

An element whose ****flow-into**** specifies a named flow takes its descendents along with it by default, with two exceptions:

-   If a descendent specifies a different named flow, it can be presented in a different series of regions specified by a corresponding [**flow-from**](/css/properties/flow-from).

-   If a descendent specifies the same named flow, it is moved from within the content and then appended.

Setting a descendent's ****flow-into**** to **none** has no effect, and cannot be used to prevent the descendent from flowing along with the ancestor.

More than one element can contribute to the same named flow, in which case their DOM order determines how they appear output within regions.

For an overview of CSS Regions, see [Using CSS Regions to flow content through a layout](/tutorials/css-regions).

## Related specifications

Specification
:   Status
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

-   [flow-from](/css/properties/flow-from)

-   **flow-into**

### External resources

-   W3C editor's draft: [CSS Regions Module Level 3](http://dev.w3.org/csswg/css3-regions/)
-   Adobe Web Standards: [CSS Regions](http://html.adobe.com/webstandards/cssregions)
-   Adobe Developer's Network: [CSS3 Regions: Rich page layout with HTML and CSS3](http://www.adobe.com/devnet/html5/articles/css3-regions.html)
-   [Sample pages](http://adobe.github.com/web-platform/samples/css-regions)
-   [Additional examples on codpen.io](http://codepen.io/collection/jabto). This experimental feature is in WebKit (Chrome and Safari) and Trident (Internet Explorer). Enable experimental features to see how CSS Regions works.

