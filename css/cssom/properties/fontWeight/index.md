---
title: fontWeight
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
summary: 'Gets or sets the weight of the font of the object.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/fontWeight_1.htm'
uri: css/cssom/properties/fontWeight
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected

---
# fontWeight

## Summary

Gets or sets the weight of the font of the object.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)</span></span>

## Syntax

``` {.js}
var fontWeightValue = declaration.fontWeight;
declaration.fontWeight = fontWeightValue;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The current state of the value of the font-weight CSS property.

## Examples

The following example demonstrates how to set the [**fontWeight**](/css/properties/font-weight) property of a **p** element. The script reads the **fontWeight** property of the [**currentStyle**](/css/cssom/currentStyle) object and displays the value in a **span** element.

``` {.html}
<body onload="setInterval('s1.innerText = p1.currentStyle.fontWeight',200)">
<p id="p1">Click the buttons below.</p>
<button onclick="p1.style.fontWeight='lighter';">Lighter</button>
<button onclick="p1.style.fontWeight='normal';">Normal</button>
<button onclick="p1.style.fontWeight='bold';">Bold</button>
<button onclick="p1.style.fontWeight='bolder';">Bolder</button>
<br>Current Weight: <span id="s1"></span>
</body>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/fontWeight_1.htm)

## Notes

The **fontWeight** property of the [**currentStyle**](/css/cssom/currentStyle) object is read-only. To set the value, use the [**fontWeight**](/css/properties/font-weight) property of the [**style**](/css/cssom/style) object. Unlike the **style** object, the **fontWeight** property of the **currentStyle** object only returns numeric values. Unlike [**fontWeight**](/css/properties/font-weight), **fontWeight** is read-only and returns only numeric values. The values for **fontWeight** are mapped to specific font variations, depending on the fonts that are installed on the user's computer. In many cases, the user cannot see the difference between different **fontWeight** settings because the system chooses the closest match.

### Syntax

`fontWeight: 100 | 200 | 300 | 400 | 500 | 600 | 700 | 800 | 900`

## See also

### Related articles

#### CSSOM

-   [href](/css/cssom/CSSImportRule/href)

-   [media](/css/cssom/CSSImportRule/media)

-   [CSSKeyframeRule](/css/cssom/CSSKeyframeRule)

-   [keyText](/css/cssom/CSSKeyframeRule/keyText)

-   [style](/css/cssom/CSSKeyframeRule/style)

-   [CSSKeyframesRule](/css/cssom/CSSKeyframesRule)

-   [cssRules](/css/cssom/CSSKeyframesRule/cssRules)

-   [deleteRule](/css/cssom/CSSKeyframesRule/deleteRule)

-   [findRule](/css/cssom/CSSKeyframesRule/findRule)

-   [insertRule](/css/cssom/CSSKeyframesRule/insertRule)

-   [name](/css/cssom/CSSKeyframesRule/name)

-   [CSSMediaList](/css/cssom/CSSMediaList/CSSMediaList)

-   [appendMedium](/css/cssom/CSSMediaList/appendMedium)

-   [deleteMedium](/css/cssom/CSSMediaList/deleteMedium)

-   [item](/css/cssom/CSSMediaList/item)

-   [mediaText](/css/cssom/CSSMediaList/mediaText)

-   [CSSMediaRule](/css/cssom/CSSMediaRule/CSSMediaRule)

-   [cssRules](/css/cssom/CSSMediaRule/cssRules)

-   [deleteRule](/css/cssom/CSSMediaRule/deleteRule)

-   [insertRule](/css/cssom/CSSMediaRule/insertRule)

-   [media](/css/cssom/CSSMediaRule/media)

-   [CSSNamespaceRule](/css/cssom/CSSNamespaceRule/CSSNamespaceRule)

-   [namespaceURI](/css/cssom/CSSNamespaceRule/namespaceURI)

-   [prefix](/css/cssom/CSSNamespaceRule/prefix)

-   [CSSOM View](/css/cssom/CSSOM_view)

-   [CSSRule](/css/cssom/CSSRule)

-   [cssText](/css/cssom/CSSRule/cssText)

-   [parentRule](/css/cssom/CSSRule/parentRule)

-   [parentStyleSheet](/css/cssom/CSSRule/parentStyleSheet)

-   [type](/css/cssom/CSSRule/type)

-   [CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)

-   [getPropertyPriority](/css/cssom/CSSStyleDeclaration/getPropertyPriority)

-   [clipLeft](/css/cssom/properties/clipLeft)

-   [clipRight](/css/cssom/properties/clipRight)

-   [clipTop](/css/cssom/properties/clipTop)

-   [cssFloat](/css/cssom/properties/cssFloat)

-   **fontWeight**

-   [hasLayout](/css/cssom/properties/hasLayout)

-   [height](/css/cssom/properties/height)

-   [href](/css/cssom/properties/href)

-   [imports](/css/cssom/properties/imports)

-   [innerWidth](/css/cssom/properties/innerWidth)

-   [isAlternate](/css/cssom/properties/isAlternate)

-   [isPrefAlternate](/css/cssom/properties/isPrefAlternate)

-   [item](/css/cssom/properties/item)

-   [length](/css/cssom/properties/length)

-   [media](/css/cssom/properties/media)

-   [offsetX](/css/cssom/properties/offsetX)

-   [offsetY](/css/cssom/properties/offsetY)

-   [outerHeight](/css/cssom/properties/outerHeight)

<!-- -->

    … further results

### Related pages (MSDN)

-   `currentStyle`
-   `defaults`
-   `Reference`
-   `fontWeight`
-   `font`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

