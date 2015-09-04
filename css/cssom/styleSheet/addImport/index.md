---
title: addImport
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
notes:
  - 'examples needed'
summary: 'Non standard. Adds an @import rule to the style sheet.'
uri: css/cssom/styleSheet/addImport

---
# addImport

## Summary

Non standard. Adds an @import rule to the style sheet.

*Method of [css/cssom/styleSheet](/css/cssom/styleSheet)*

## Syntax

``` {.js}
var index = stylesheet.addImport(/* see parameter list */);
```

## Parameters

### url

 Data-typeÂ
:   String

 The location of the source file for the style sheet.

### index

 Data-typeÂ
:   Number

*(Optional)*

The requested position for the style sheet in the collection. If this value is not given, the style sheet is added to the end of the collection.

## Return Value

Returns an object of type Number.

A zero-based index value indicating the position of the imported style sheet in the [**imports**](/css/cssom/imports) collection.

**Needs Examples**: This section should include examples.

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

-   [fontWeight](/css/cssom/properties/fontWeight)

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

    â€¦ further results

### Related pages (MSDN)

-   `IHTMLStyleSheet`
-   `styleSheet`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

