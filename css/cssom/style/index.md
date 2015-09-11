---
title: style
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary needed. double check token printing in standards section.'
readiness: 'In Progress'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: CSSStyleDeclaration
    href: /css/cssom/CSSStyleDeclaration/CSSStyleDeclaration
standardization_status: 'W3C Recommendation'
summary: 'The style attribute of an element makes it possible to directly apply CSS-styles to that specific element.'
tags:
  - Pages
  - using
  - duplicate
  - arguments
  - in
  - template
  - calls
  - API
  - Objects
  - DOM
uri: css/cssom/style

---
## <span>Summary</span>

The style attribute of an element makes it possible to directly apply CSS-styles to that specific element.

Inherits from [CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)

## <span>Properties</span>

API Name
:   Summary

[type](/css/cssom/style/type)
:

## <span>Methods</span>

*No methods.*

## <span>Events</span>

*No events.*

## <span>Inherited from CSSStyleDeclaration</span>

### <span>Properties</span>

API Name
:   Summary

[cssText](/css/cssom/CSSStyleDeclaration/cssText)
:   Gets or sets the textual representation of a CSS style declaration.

[item](/css/cssom/CSSStyleDeclaration/item)
:

[background](/css/cssom/properties/background)
:   The background-position property sets the starting position of a background image.

[clipBottom](/css/cssom/properties/clipBottom)
:   Gets the bottom coordinate of the object clipping region.

[clipRight](/css/cssom/properties/clipRight)
:

[clipTop](/css/cssom/properties/clipTop)
:

[cssFloat](/css/cssom/properties/cssFloat)
:

[fontWeight](/css/cssom/properties/fontWeight)
:   Gets or sets the weight of the font of the object.

[hasLayout](/css/cssom/properties/hasLayout)
:

[height](/css/cssom/properties/height)
:   Sets the height of an element.

[width](/css/cssom/properties/width)
:   Sets the width of an element.

### <span>Methods</span>

API Name
:   Summary

[getPropertyPriority](/css/cssom/CSSStyleDeclaration/getPropertyPriority)
:   Gets the priority of a property in a CSS style declaration.

[getPropertyValue](/css/cssom/CSSStyleDeclaration/getPropertyValue)
:   Gets the value of a property in a CSS style declaration.

[removeProperty](/css/cssom/CSSStyleDeclaration/removeProperty)
:   Removes a property from a CSS style declaration.

[msGetPropertyEnabled](/css/cssom/methods/msGetPropertyEnabled)
:   Non standard. Indicates whether a property is enabled.

[msPutPropertyEnabled](/css/cssom/methods/msPutPropertyEnabled)
:   Non standard. Sets a property as enabled or disabled.

### <span>Events</span>

*No events.*

## <span>Examples</span>

This example uses the **style** object to set the document body text font to Verdana.

``` js
document.body.style.fontFamily = "Verdana"
```

This example positions all absolutely positioned images in the given document at the top of the document.

``` js
var oImages = document.all.tags("IMG");
if (oImages.length) {
    for (var iImg = 0; iImg < oImages.length; iImg++) {
        var oImg = oImages(iImg);
        if (oImg.style.position == "absolute") {
            oImg.style.top = 0;
        }
    }
}
```

This example copies the inline style of the second element (`div2`) to the first (`div1`) while preserving the styles of the second. The background color of `div1` is overwritten during the assignment.

``` js
<DIV ID="div1" STYLE="background-color:blue;font-weight:bold">Item 1</DIV>
<DIV ID="div2" STYLE="background-color:red;font-size:18pt;
    font-family:Verdana;">Item 2</DIV>
<SCRIPT>
div1.style.cssText += (';' + div2.style.cssText);
</SCRIPT>
```

## <span>Notes</span>

### <span>Remarks</span>

Inline styles are CSS assignments that you apply directly to individual HTML elements using the [**STYLE**](/html/attributes/STYLE_html_attribute) attribute. Use the **style** object to examine these assignments and to make new assignments or change existing ones. To retrieve the **style** object, apply the **style** keyword to an `element` object. To retrieve the current setting for an inline style, apply the corresponding **style** property to the **style** object. The **style** object does not provide access to the style assignments in style sheets. To obtain information about styles in style sheets, use the [**styleSheets**](/css/cssom/styleSheets) collection to access to the individual style sheets defined in the document. The following properties are not available when the [**rule**](/css/cssom/rule) object accesses the **style** object: [**posHeight**](/css/cssom/properties/posHeight), [**posWidth**](/css/cssom/properties/posWidth), [**posTop**](/css/cssom/properties/posTop), [**posLeft**](/css/cssom/properties/posLeft), [**pixelHeight**](/css/cssom/properties/pixelHeight), [**pixelWidth**](/css/cssom/properties/pixelWidth), [**pixelTop**](/css/cssom/properties/pixelTop), and [**pixelLeft**](/css/cssom/properties/pixelLeft). To change or clear multiple style properties simultaneously, use this object with the [**cssText**](/css/cssom/styleSheet/cssText) property. For example, to change the font color and background color of a **DIV** element, you could use the following code:

    <DIV onclick="this.style.cssText = 'color:red;background-color:blue;border:5px solid black;'">
    Click this DIV to change style properties.</DIV>

### <span>Standards information</span>

There are no standards that apply here.

### <span>Members</span>

The **style** object has these types of members:

-   [\#methods Methods]
-   [\#properties Properties]

#### <span>Methods</span>

The **style** object has these methods.

{

## <span>Related specifications</span>

[CSS Style Attributes](http://www.w3.org/TR/css-style-attr/)
:   Recommendation

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

-   [pageY](/css/cssom/properties/pageY)

-   [pageYOffset](/css/cssom/properties/pageYOffset)

-   [pixelBottom](/css/cssom/properties/pixelBottom)

-   [deviceXDPI](/css/cssom/screen/deviceXDPI)

-   [deviceYDPI](/css/cssom/screen/deviceYDPI)

-   [fontSmoothingEnabled](/css/cssom/screen/fontSmoothingEnabled)

-   [height](/css/cssom/screen/height)

-   **style**

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
