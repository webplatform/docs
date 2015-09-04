---
title: removeRule
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Not Ready'
notes:
  - 'Non-standard; deletion candidate'
summary: 'Non standard. Removes a rule from a style sheet.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/removeRule.htm'
uri: css/cssom/stylesheet/removeRule

---
# removeRule

## Summary

Non standard. Removes a rule from a style sheet.

*Method of [css/cssom/styleSheet](/css/cssom/styleSheet)*

## Syntax

``` {.js}
 stylesheet.removeRule(index);
```

## Parameters

### index

 Data-typeÂ
:   Number

 The index value of the rule to be deleted from the style sheet. If an index is not provided, the first rule in the [**rules**](/css/cssom/rules) collection is removed.

## Return Value

No return value

## Examples

This example uses the **removeRule** method to delete a rule from the [**rules**](/css/cssom/rules) collection, which causes the text to reflow according to the new rules.

``` {.html}
<style>
P {color:green}
</style>
:
<script>
function removeTheRule() {
    // Style sheets and rules are zero-based collections; therefore,
    // the first item is item 0 in the collection.
    var iSheets = document.styleSheets.length;
    var iRules = document.styleSheets[iSheets-1].rules.length;
    // make sure there is a rule to delete
    if (1 < iRules) {
        document.styleSheets[iSheets-1].removeRule(1);
        // Force the page to render the change.
        effectRules = document.getElementById("oEffectRules");
        effectRules.innerHTML = effectRules.innerHTML;
    }
}
</script>
:
<p id="oEffectRules">This text has the new style applied to it.
</p>
:
<button onclick="removeTheRule()">Remove the new rule.</button>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/removeRule.htm)

## Notes

### Remarks

The document does not automatically reflow when the rule is removed. To see the change, you must reflow the document. You can reflow the objects affected using a number of methods. For example, you can reflow the style change only on affected text by setting the text equal to itself. Alternately, you can reload the entire document using the [**reload**](/dom/Location/reload) method. When you use the **refresh** method on a table, its content is reflowed.

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
-   `Reference`
-   `addRule`
-   `rules`
-   `styleSheets`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

