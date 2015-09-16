---
title: 'pageY'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary and examples needed.'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/objects/MouseEvent
    href: '/w/index.php?title=dom/objects/MouseEvent&action=edit&redlink=1'
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: '/w/index.php?title=dom/objects/MouseEvent&action=edit&redlink=1'
standardization_status: 'W3C Working Draft'
summary: 'Gets the y-coordinate of the mouse cursor, relative to the upper-left corner of the page.'
tags:
  - API
  - Object
  - Properties
  - DOM
  - DOMEvents
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/objects/MouseEvent
    - dom/properties/clientY
    - dom/properties/scrollTop
    - dom/objects/DragEvent
    - dom/objects/MouseWheelEvent
    - dom/objects/WheelEvent
    - dom/properties/screenY
uri: css/cssom/properties/pageY

---
## Summary

Gets the y-coordinate of the mouse cursor, relative to the upper-left corner of the page.

Property of [dom/objects/MouseEvent](/w/index.php?title=dom/objects/MouseEvent&action=edit&redlink=1)[dom/objects/MouseEvent](/w/index.php?title=dom/objects/MouseEvent&action=edit&redlink=1)

## Syntax

**Note**: This property is read-only.

``` js
var yCoordinate = event.pageY;
```

## Return Value

Returns an object of type NumberNumber

The Y coordinate of the mouse cursor.

**Needs Examples**: This section should include examples.

## Notes

The **pageY** property is equivalent to the [**clientY**](/w/index.php?title=dom/properties/clientY&action=edit&redlink=1) value plus the [**scrollTop**](/w/index.php?title=dom/properties/scrollTop&action=edit&redlink=1) value of the document, as the following code example shows.

    var pageY = event.clientY + document.documentElement.scrollTop;

## Related specifications

[CSSOM View](http://www.w3.org/TR/cssom-view/)
:   Working Draft

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

-   [parentStyleSheet](/css/cssom/CSSRule/parentStyleSheet)

-   [type](/css/cssom/CSSRule/type)

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

-   [outerWidth](/css/cssom/properties/outerWidth)

-   [pageX](/css/cssom/properties/pageX)

-   [pageXOffset](/css/cssom/properties/pageXOffset)

-   **pageY**

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

### Related pages

-   DragEvent[DragEvent](/w/index.php?title=dom/objects/DragEvent&action=edit&redlink=1)
-   MouseWheelEvent[MouseWheelEvent](/w/index.php?title=dom/objects/MouseWheelEvent&action=edit&redlink=1)
-   WheelEvent[WheelEvent](/w/index.php?title=dom/objects/WheelEvent&action=edit&redlink=1)
-   `Reference`
-   clientY[clientY](/w/index.php?title=dom/properties/clientY&action=edit&redlink=1)
-   offsetY[offsetY](/css/cssom/properties/offsetY)
-   screenY[screenY](/w/index.php?title=dom/properties/screenY&action=edit&redlink=1)
-   y[y](/css/cssom/properties/y)
