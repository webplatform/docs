---
title: @region
tags:
  - CSS
  - At
  - Rules
  - CSS-Regions
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Applies CSS styles to portions of content as it appears when flowing within a specified set of regions.'
uri: css/atrules/@region

---
# @region

## Summary

Applies CSS styles to portions of content as it appears when flowing within a specified set of regions.

 The basic syntax is as follows:

``` {.css}
 @region <region_selector> {
     <content_selector> {
         /* ... CSS properties ... */
     }
 }
```

 The *region\_selector* specifies a set of region elements. Within that scope, the *content\_selector* applies to any [*range*](/css/concepts/fragment) (or 'fragment') of the selected content when it appears within each region. This example produces the following result:

``` {.css}
 /* default paragraph text */
 p { color: gray: }

 /* customized for fragments that appear within region */
 @region-style #intro {
     p { color: blue; }
 }
```

 ![regionRule2.jpeg](/assets/public/5/5c/regionRule2.jpeg)

## Examples

Inverts paragraph text within the first region

``` {.css}
/* dark gray text color by default */
p {
    color: #444;
}

/* dark gray background for first region */
div.region:first-of-type {
    background-color: #444;
}

/* white text only within first region */
@region div.region:first-of-type {
    p {
        color: #fff;
    }
}

/* associate content with CSS regions */
article.content { flow-into: main; }
div.region { flow-from: main; }
```

## Usage

     The @region rule does not change the cascading order of content selectors.

Use the [**CSSRegionStyleRule**](/apis/css-regions/CSSRegionStyleRule) interface to apply **@region** rules programmatically.

## Notes

Only the following set of CSS properties work within **@region** rules:

-   font properties ([**font-weight**](/css/properties/font-weight), [**font-size**](/css/properties/font-size), [**font-variant**](/css/properties/font-variant), [**font-style**](/css/properties/font-style), [**font-family**](/css/properties/font-family))
-   [**color**](/css/properties/color)
-   [**opacity**](/css/properties/opacity)
-   background properties ([**background-color**](/css/properties/background-color), [**background-image**](/css/properties/background-image))
-   alignment and justification properties ([**text-align**](/css/properties/text-align), [**text-align-last**](/css/properties/text-align-last), [**word-spacing**](/css/properties/word-spacing), [**text-justify**](/css/properties/text-justify))
-   [**letter-spacing**](/css/properties/letter-spacing)
-   [**text-decoration**](/css/properties/text-decoration)
-   [**text-transform**](/css/properties/text-transform)
-   [**line-height**](/css/properties/line-height)
-   border properties ([**border-color**](/css/properties/border-color), [**border-style**](/css/properties/border-style), [**border-width**](/css/properties/border-width))
-   [**border-radius**](/css/properties/border-radius)
-   border image properties: ([**border-image-source**](/css/properties/border-image-source), [**border-image-slice**](/css/properties/border-image-slice), [**border-image-width**](/css/properties/border-image-width), [**border-image-outset**](/css/properties/border-image-outset), [**border-image-repeat**](/css/properties/border-image-repeat))
-   [**margin**](/css/properties/margin)
-   [**padding**](/css/properties/padding)
-   [**text-shadow**](/css/properties/text-shadow)
-   [**box-shadow**](/css/properties/box-shadow)
-   [**box-decoration-break**](/css/properties/box-decoration-break)
-   [**width**](/css/properties/width)

## Related specifications

Specification
:   Status
[CSS Regions Module Level 1](http://www.w3.org/TR/2012/WD-css3-regions-20120823/)
:   W3C Working Draft 23 August 2012

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

-   **@region**

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

