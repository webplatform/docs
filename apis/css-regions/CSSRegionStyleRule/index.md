---
title: CSSRegionStyleRule
readiness: 'Ready to Use'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: CSSRule
    href: /css/cssom/CSSRule
standardization_status: 'W3C Working Draft'
summary: 'Represents an @region rule in a CSS style sheet, which applies styles to fragments of content that flow into a CSS region.'
tags:
  0: API
  1: Objects
  3: CSS-Regions
uri: apis/css-regions/CSSRegionStyleRule

---
## <span>Summary</span>

Represents an @region rule in a CSS style sheet, which applies styles to fragments of content that flow into a CSS region.

Inherits from [CSSRule](/css/cssom/CSSRule)[CSSRule](/css/cssom/CSSRule)

## <span>Properties</span>

*No properties.*

## <span>Methods</span>

*No methods.*

## <span>Events</span>

*No events.*

## <span>Inherited from CSSRule</span>

### <span>Properties</span>

API Name
:   Summary

[cssText](/css/cssom/CSSRule/cssText)
:   Gets or sets a textual representation of a CSS rule.

[parentStyleSheet](/css/cssom/CSSRule/parentStyleSheet)
:

[type](/css/cssom/CSSRule/type)
:

### <span>Methods</span>

*No methods.*

### <span>Events</span>

*No events.*

## <span>Examples</span>

Starting with this CSS...

``` css
@region div.region {
    p {
    color: #fff;
        background-color: #000;
    }
}
```

Narrow the scope of the first rule within the @region to the first paragraph, and modify its background color

``` js
// corresponds to @region rule above:
rule = document.styleSheets[0].cssRules[0];

// modify first nested style's selector:
rule.cssRules[0].selectorText = 'article > p:first-of-type';

// modify first nested style's background-color property:
rule.cssRules[0].style.backgroundColor = '#777';

// inspect first nested style as read-only string:
console.log(rule.cssRules[0].cssText);

// inspect CSS syntax for entire @region rule:
console.log(rule.cssText);
```

The **cssText** above now dynamically reflects these altered values:

``` css
@region div.region {
    p:first-of-type {
    color: #fff;
        background-color: #777;
    }
}
```

## <span>Related specifications</span>

[CSS Regions Module Level 1](http://www.w3.org/TR/2012/WD-css3-regions-20120823/)
:   W3C Working Draft 23 August 2012

## <span>See also</span>

### <span>Related articles</span>

#### <span>Regions</span>

-   [CSS Regions API](/apis/css-regions)

-   **CSSRegionStyleRule**

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

-   [flow-into](/css/properties/flow-into)

### <span>External resources</span>

-   W3C editor's draft: [CSS Regions Module Level 3](http://dev.w3.org/csswg/css3-regions/)
-   Adobe Web Standards: [CSS Regions](http://html.adobe.com/webstandards/cssregions)
-   Adobe Developer's Network: [CSS3 Regions: Rich page layout with HTML and CSS3](http://www.adobe.com/devnet/html5/articles/css3-regions.html)
-   [Sample pages](http://adobe.github.com/web-platform/samples/css-regions)
