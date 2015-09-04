---
title: cssText
tags:
  0: API
  1: Object
  2: Properties
  4: CSS
  5: CSS-Regions
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Gets or sets a textual representation of a CSS rule.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/css/cssText/cssText.html'
uri: css/cssom/CSSRule/cssText

---
# cssText

## Summary

Gets or sets a textual representation of a CSS rule.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/cssom/CSSRule/CSSRule](/css/cssom/CSSRule/CSSRule)</span></span>

## Syntax

``` {.js}
var ruleText = rule.cssText;
rule.cssText = ruleText;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

Returns a textual representation of a CSS rule.

## Examples

``` {.html}
<div id="myDiv"></div>
<input type="button" value="Blue" id="blueButton">
<input type="button" value="Red" id="redButton">
<script>
    redButton.onclick=function(){
        //create a css style using cssText
        myDiv.style.cssText = "background-image: radial-gradient(red,  yellow); color: darkred;"

        // write the cssText to the contents of the div
        myDiv.innerHTML = "The cssText value is: " + myDiv.style.cssText;
    }
    blueButton.onclick=function(){
        //create a css style using cssText
        myDiv.style.cssText = "background-image: radial-gradient(blue,  white); color: darkblue;"

        // write the cssText to the contents of the div
        myDiv.innerHTML = "The cssText value is: " + myDiv.style.cssText;
    }
</script>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/css/cssText/cssText.html)

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

-   **cssText**

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

