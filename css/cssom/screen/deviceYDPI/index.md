---
title: deviceYDPI
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
notes:
  - 'Needs spec reference, standardization status'
summary: 'Retrieves the device''s vertical Dots Per Inch (DPI) value.'
uri: css/cssom/screen/deviceYDPI

---
# deviceYDPI

## Summary

Retrieves the device's vertical Dots Per Inch (DPI) value.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/cssom/screen](/css/cssom/screen)</span></span>

## Syntax

``` {.js}
var result = element.deviceYDPI;
element.deviceYDPI = value;
```

## Examples

The following examples use the **deviceYDPI** property to retrieve the vertical DPI of the screen. The function in this example returns `1` if Internet Explorer is not adjusting the scale of the screen.

``` {.js}
<script>
  function fnScaleFactorY() {
    var nScaleFactor = screen.deviceYDPI / screen.logicalYDPI;
    return nScaleFactor;
  }
</script>
```

This example uses the [**-ms-zoom**](/css/selectors/zoom) property of the **BODY** element to adjust the scale of the document "manually" if Internet Explorer is not adjusting the scale of the screen and the user's vertical DPI is higher than normal. This is a simple but imprecise way to make a document look the same on higher resolution screens. You can achieve finer control over the layout of your documents by modifying the properties of individual elements or groups of elements.

``` {.js}
<script>
  // change layout on HighDPI screens when IE not scaling
  function fnScaleManually()
  {
    // normal DPI
    var constNorm = 96;

    // scaling is off and DPI higher than normal
    if ((screen.deviceYDPI == screen.logicalYDPI)
      && (screen.deviceYDPI > constNorm))
    {
      document.body.style.zoom =
        constNorm / screen.logicalYDPI;
    }
  }
</script>
```

## Notes

### Remarks

On most systems, there is no difference between horizontal and vertical DPI. The **deviceYDPI** property was introduced in Microsoft Internet Explorer 6. For information about how Internet Explorer 6 and later can adjust the scale of the display on screens with higher-than-normal DPI, see Adjusting Scale for Higher DPI Screens.

### Syntax

### Standards information

There are no standards that apply here.

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

-   `screen`
-   `Reference`
-   `deviceXDPI`
-   `logicalXDPI`
-   `logicalYDPI`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

