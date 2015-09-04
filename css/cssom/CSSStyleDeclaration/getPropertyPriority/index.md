---
title: getPropertyPriority
tags:
  - API
  - Object
  - Methods
  - CSS
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Gets the priority of a property in a CSS style declaration.'
uri: css/cssom/CSSStyleDeclaration/getPropertyPriority

---
# getPropertyPriority

## Summary

Gets the priority of a property in a CSS style declaration.

*Method of [css/cssom/CSSStyleDeclaration/CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)*

## Syntax

``` {.js}
var priority = declaration.getPropertyPriority(property);
```

## Parameters

### property

 Data-typeÂ
:   String

 The name of the CSS property.

## Return Value

Returns an object of type String.

A string that represents the priority if the property is explicitly set in this declaration block and has a specified priority specified, or null.

## Examples

Gets the priority of the first rule in the stylesheet.

``` {.html}
<head>
<style>
#aDiv {
    width:200px !important;
}
</style>
<script type="text/javascript">
var rule = document.styleSheets[0].cssRules[0];
var priority = rule.style.getPropertyPriority ("width");
alert (priority);
</script>
</head>

<body>
This is a div.
</body>
```

## Notes

The priority of a CSS property is designated by, for example, the [!important](/css/syntax/!important) declaration.

## Related specifications

Specification
:   Status
[DOM Level 2 Style](http://www.w3.org/TR/2000/REC-DOM-Level-2-Style-20001113/css.html)
:   Recommendation

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

-   **getPropertyPriority**

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

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `style`
-   `Reference`
-   `getPropertyValue`
-   `item`
-   `length`
-   `removeProperty`
-   `setProperty`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

