---
title: clipBottom
tags:
  - API
  - Object
  - Properties
  - CSS
readiness: 'Ready to Use'
summary: 'Gets the bottom coordinate of the object clipping region.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clipBottom.htm'
uri: css/cssom/properties/clipBottom

---
# clipBottom

## Summary

Gets the bottom coordinate of the object clipping region.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)</span></span>

## Syntax

``` {.js}
var result = declaration.clipBottom;
declaration.clipBottom = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

## Examples

This example reads the **clipBottom** property from the [**currentStyle**](/css/cssom/currentStyle) object of an image.

``` {.html}
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

### Related pages (MSDN)

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `style`
-   `Reference`
-   `clip`
-   `clipLeft`
-   `clipRight`
-   `clipTop`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

