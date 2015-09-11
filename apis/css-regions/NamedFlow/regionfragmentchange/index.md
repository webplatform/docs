---
title: regionfragmentchange
code_samples:
  - 'http://letmespellitoutforyou.com/samples/region_fragmentchange.html'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Fires on the  NamedFlow object when there is a change in how content flows through a region chain.'
tags:
  - Events
  - API
  - CSS
  - CSS-Regions
uri: apis/css-regions/NamedFlow/regionfragmentchange

---
## <span>Summary</span>

Fires on the NamedFlow object when there is a change in how content flows through a region chain.

## <span>Overview Table</span>

<table class="wikitable">
<tr>
<th>
Synchronous

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Bubbles

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Target

</th>
<td>
[**NamedFlow**](/apis/css-regions/NamedFlow)

</td>
</tr>
<tr>
<th>
Cancelable

</th>
<td>
Yes

</td>
</tr>
<tr>
<th>
Default action

</th>
<td>
none

</td>
</tr>
</table>
Fires on the [**NamedFlow**](/apis/css-regions/NamedFlow) object when there is 'any' change in how content flows through a [region chain](/css/concepts/region_chain), even minor changes that don't affect the total number of [regions](/css/concepts/region) the content requires.

## <span>Examples</span>

This simple example logs each time content reflows among regions, and works with the CSS and JavaScript that follow. Define layout and content elements:

``` html
<html>
<body>
<section class="page">
    <div> <h1>Region #1</h1> </div>
    <div> <h1>Region #2</h1> </div>
    <aside></aside>
</section>
<article>
<h1>Sample CSS Regions Layout</h1>
<p>Riverrun, past Eve and Adam's, from swerve of shore to bend of bay, brings us by a commodius vicus of recirculation back to Howth Castle and Environs.</p>
<p>...</p>
</article>
</body>
</html>
```

[View live example](http://letmespellitoutforyou.com/samples/region_fragmentchange.html)

Flow the content into the layout:

``` css
body { background: #aaa; }
article { flow-into: main; }

div {
    flow-from: main;
    region-fragment: break;
    top: 5%;
    width: 40%;
    height: 75%;
}

div, aside {
    position: absolute;
    background: #fff;
    padding: 1em;
    border-radius: 1em;
}

aside {
    min-width: 40%;
    left: 5%;
    top: 90%;
}

div:first-of-type { left: 5%; }
div:last-of-type { left: 55%; }
```

[View live example](http://letmespellitoutforyou.com/samples/region_fragmentchange.html)

Log to console any shifts of content from one region to another that result when resizing the window, and thus the layout elements.

``` js
document.getNamedFlows().namedItem('main').addEventListener(
    'regionfragmentchange',
    function() { console.log(inc++); }
);
```

[View live example](http://letmespellitoutforyou.com/samples/region_fragmentchange.html)

## <span>Notes</span>

The event fires when content shifts 'in any way' within the [region chain](/css/concepts/region_chain), such as when linebreaks change. That is, when any [region's](/css/concepts/region) [collection of DOM Range fragments](/apis/css-regions/Region/getRegionFlowRanges) changes their dimensions or offsets. (Compare with the [**regionoversetchange**](/apis/css-regions/NamedFlow/regionoversetchange) event, which fires much less frequently in response to changing content or dimensions.)

## <span>Related specifications</span>

[CSS Regions Module Level 1](http://www.w3.org/TR/css3-regions/)
:   W3C Working Draft

## <span>See also</span>

### <span>Related articles</span>

#### <span>Regions</span>

-   [CSS Regions API](/apis/css-regions)

-   [CSSRegionStyleRule](/apis/css-regions/CSSRegionStyleRule)

-   [NamedFlow](/apis/css-regions/NamedFlow)

-   [firstEmptyRegionIndex](/apis/css-regions/NamedFlow/firstEmptyRegionIndex)

-   [getContent()](/apis/css-regions/NamedFlow/getContent)

-   [getRegions()](/apis/css-regions/NamedFlow/getRegions)

-   [getRegionsByContent()](/apis/css-regions/NamedFlow/getRegionsByContent)

-   [name](/apis/css-regions/NamedFlow/name)

-   [overset](/apis/css-regions/NamedFlow/overset)

-   **regionfragmentchange**

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
