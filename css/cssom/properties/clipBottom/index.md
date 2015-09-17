---
title: 'clipBottom'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clipBottom.htm'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/cssom/CSSStyleDeclaration/CSSStyleDeclaration
    href: /css/cssom/CSSStyleDeclaration/CSSStyleDeclaration
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /css/cssom/CSSStyleDeclaration/CSSStyleDeclaration
summary: 'Gets the bottom coordinate of the object clipping region.'
tags:
  - API_Object_Properties
  - CSS
uri: css/cssom/properties/clipBottom

---
## Summary

Gets the bottom coordinate of the object clipping region.

Property of [css/cssom/CSSStyleDeclaration/CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)

## Syntax

``` js
var result = declaration.clipBottom;
declaration.clipBottom = value;
```

## Return Value

Returns an object of type StringString

## Examples

This example reads the **clipBottom** property from the [**currentStyle**](/css/cssom/currentStyle) object of an image.

``` html
<SCRIPT>
function setClip(sOptionValue) {
    oImage.style.clip="rect(0,100,"+sOptionValue+",0)";
    if (oImage.currentStyle.clipBottom == "60px") {
        alert("The image has been clipped to 60px.");
        }
:
}
</SCRIPT>
:
<IMG ID=oImage SRC="/workshop/graphics/sphere.png">
:
Pick an amount to clip the bottom:
    // the option value is sent as an argument:
<SELECT onchange="setClip(value)">
<OPTION VALUE=100>reset </OPTION>
<OPTION VALUE=40>40px </OPTION>
<OPTION VALUE=50>50px </OPTION>
<OPTION VALUE=60>60px </OPTION>
</SELECT>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clipBottom.htm)

## See also

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   style[style](/css/cssom/style)
-   `Reference`
-   clip[clip](/css/properties/clip)
-   clipLeft[clipLeft](/css/cssom/properties/clipLeft)
-   clipRight[clipRight](/css/cssom/properties/clipRight)
-   clipTop[clipTop](/css/cssom/properties/clipTop)
