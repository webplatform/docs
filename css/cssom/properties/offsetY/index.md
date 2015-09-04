---
title: offsetY
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
notes:
  - 'some broken links, readable though.'
summary: 'Gets the y-coordinate of the mouse cursor, relative to the target node.'
uri: css/cssom/properties/offsetY
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/objects/MouseEvent
    - dom/properties/offsetLeft
    - dom/properties/offsetTop
    - dom/properties/offsetParent
    - dom/objects/DragEvent
    - dom/objects/MouseWheelEvent
    - dom/objects/WheelEvent
    - dom/properties/clientY
    - dom/properties/screenY

---
# offsetY

## Summary

Gets the y-coordinate of the mouse cursor, relative to the target node.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/objects/MouseEvent](/w/index.php?title=dom/objects/MouseEvent&action=edit&redlink=1)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var yCoordinate = event.offsetY;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

The Y coordinate of the mouse cursor.

## Examples

This example uses the **offsetY** property to determine the mouse position relative to the container that fired the event, and also displays the mouse coordinates in the console.

``` {.html}
<!doctype html>
<html>
 <head>
  <style>
#div {
  position:absolute;
  top:200px;
  left:300px;
}
  </style>
  <script>
function offsetCoords(e) {
  var offsetInfo = ""
  offsetInfo = "The x coordinate is: " + e.offsetX + "\n"
  offsetInfo += "The y coordinate is: " + e.offsetY + "\r"
  console.log(offsetInfo);
}
function logCoords(e) {
  console.log("X = " + e.offsetX + " Y = " + e.offsetY);
}
function initialize() {
  document.body.addEventListener("mousemove", logCoords, false);
  document.body.addEventListener("click", offsetCoords, false);
  document.getElementById("div").addEventListener("click", offsetCoords, false);
}
window.addEventListener("load", initialize, false);
  </script>
 </head>
 <body>
  <div id="div">
  </div>
 </body>
</html>
```

## Notes

Offset coordinates include the padding of an element, but not its margin or border.

**TODO**: Check that this is correct.

The coordinates match the [**offsetLeft**](/w/index.php?title=dom/properties/offsetLeft&action=edit&redlink=1) and [**offsetTop**](/w/index.php?title=dom/properties/offsetTop&action=edit&redlink=1) properties of the object. Use [**offsetParent**](/w/index.php?title=dom/properties/offsetParent&action=edit&redlink=1) to find the container object that defines this coordinate system.

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

-   **offsetY**

-   [outerHeight](/css/cssom/properties/outerHeight)

<!-- -->

    … further results

### Related pages (MSDN)

-   `DragEvent`
-   `MouseEvent`
-   `MouseWheelEvent`
-   `WheelEvent`
-   `Reference`
-   `clientY`
-   `pageY`
-   `screenY`
-   `y`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

