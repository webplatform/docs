---
title: pageX
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'needs examples.'
summary: 'Gets the x-coordinate of the mouse cursor, relative to the upper-left corner of the page.'
uri: css/cssom/properties/pageX
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/objects/MouseEvent
    - dom/properties/clientX
    - dom/properties/scrollLeft
    - dom/objects/DragEvent
    - dom/objects/MouseWheelEvent
    - dom/objects/WheelEvent
    - dom/properties/screenX

---
# pageX

## Summary

Gets the x-coordinate of the mouse cursor, relative to the upper-left corner of the page.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/objects/MouseEvent](/w/index.php?title=dom/objects/MouseEvent&action=edit&redlink=1)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var xCoordinate = event.pageX;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

The X coordinate of the mouse cursor.

**Needs Examples**: This section should include examples.

## Notes

The **pageX** property is equivalent to the [**clientX**](/w/index.php?title=dom/properties/clientX&action=edit&redlink=1) value plus the [**scrollLeft**](/w/index.php?title=dom/properties/scrollLeft&action=edit&redlink=1) value of the document, as the following code example shows.

    var pageX = event.clientX + document.documentElement.scrollLeft;

## Related specifications

Specification
:   Status
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

    … further results

### Related pages (MSDN)

-   `DragEvent`
-   `MouseWheelEvent`
-   `WheelEvent`
-   `Reference`
-   `clientX`
-   `offsetX`
-   `screenX`
-   `x`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

