---
title: height
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'syntax section empty or dupe header'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/cssom/CSSStyleDeclaration/CSSStyleDeclaration
    href: /css/cssom/CSSStyleDeclaration/CSSStyleDeclaration
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /css/cssom/CSSStyleDeclaration/CSSStyleDeclaration
standardization_status: 'W3C Recommendation'
summary: 'Sets the height of an element.'
tags:
  - API
  - Object
  - Properties
  - DOM
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/traversal/properties/top
    - dom/properties/bottom
uri: css/cssom/properties/height

---
## <span>Summary</span>

Sets the height of an element.

Property of [css/cssom/CSSStyleDeclaration/CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)

## <span>Syntax</span>

``` js
var result = declaration.height;
declaration.height = value;
```

## <span>Return Value</span>

Returns an object of type StringString

## <span>Examples</span>

Sets the height of paragraph elements to 200 px.

``` css
p { height: 200 px; }
```

## <span>Notes</span>

### <span>Remarks</span>

The height of the rectangle can also be calculated by subtracting the value of the [**top**](/w/index.php?title=dom/traversal/properties/top&action=edit&redlink=1) property from the value of the [**bottom**](/w/index.php?title=dom/properties/bottom&action=edit&redlink=1) property.

### <span>Syntax</span>

### <span>Standards information</span>

-   [CSSOM View Module](http://go.microsoft.com/fwlink/p/?linkid=199793)

## <span>See also</span>

### <span>Related articles</span>

#### <span>CSSOM</span>

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

-   [parentStyleSheet](/css/cssom/CSSRule/parentStyleSheet)

-   [type](/css/cssom/CSSRule/type)

-   [getPropertyPriority](/css/cssom/CSSStyleDeclaration/getPropertyPriority)

-   [clipLeft](/css/cssom/properties/clipLeft)

-   [clipRight](/css/cssom/properties/clipRight)

-   [clipTop](/css/cssom/properties/clipTop)

-   [cssFloat](/css/cssom/properties/cssFloat)

-   [fontWeight](/css/cssom/properties/fontWeight)

-   [hasLayout](/css/cssom/properties/hasLayout)

-   **height**

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

-   [outerWidth](/css/cssom/properties/outerWidth)

-   [pageX](/css/cssom/properties/pageX)

-   [pageXOffset](/css/cssom/properties/pageXOffset)

-   [pageY](/css/cssom/properties/pageY)

-   [pageYOffset](/css/cssom/properties/pageYOffset)

-   [pixelBottom](/css/cssom/properties/pixelBottom)

-   [deviceXDPI](/css/cssom/screen/deviceXDPI)

-   [deviceYDPI](/css/cssom/screen/deviceYDPI)

-   [fontSmoothingEnabled](/css/cssom/screen/fontSmoothingEnabled)

-   [height](/css/cssom/screen/height)

-   [style](/css/cssom/style)

-   [type](/css/cssom/style/type)

-   [styleSheet](/css/cssom/styleSheet)

-   [addImport](/css/cssom/styleSheet/addImport)

-   [blockDirection](/css/cssom/styleSheet/blockDirection)

-   [cssRules](/css/cssom/styleSheet/cssRules)

-   [cssText](/css/cssom/styleSheet/cssText)

-   [ownerNode](/css/cssom/styleSheet/ownerNode)

-   [removeImport](/css/cssom/stylesheet/removeImport)

-   [removeRule](/css/cssom/stylesheet/removeRule)

-   [matchMedium](/css/media_queries/apis/matchMedium)

-   [getComputedStyle](/dom/Window/getComputedStyle)

-   [innerHeight](/dom/Window/innerHeight)

-   [styleMedia](/dom/Window/styleMedia)
