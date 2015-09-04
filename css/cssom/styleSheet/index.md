---
title: styleSheet
tags:
  - API
  - Objects
  - DOM
readiness: 'Ready to Use'
summary: 'A style sheet in the document.'
uri: css/cssom/styleSheet
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/methods/fireEvent

---
# styleSheet

## Summary

A style sheet in the document.

## Properties

API Name
:   Summary
[cssRules](/css/cssom/styleSheet/cssRules)
:   Gets a list of CSS rules of a style sheet.
[cssText](/css/cssom/styleSheet/cssText)
:   Gets or sets the textual representation of a style sheet.
[ownerNode](/css/cssom/styleSheet/ownerNode)
:   Returns an element's corresponding **link** or **style** node. See Notes.
[ownerRule](/css/cssom/styleSheet/ownerRule)
:   Gets the CSS Rule that imported the style sheet, if any.
[owningElement](/css/cssom/styleSheet/owningElement)
:   Non standard. Returns the **style** or **link** object that defined the style sheet.
[pages](/css/cssom/styleSheet/pages)
:
[parentStyleSheet](/css/cssom/styleSheet/parentStyleSheet)
:   Retrieves an element's parent style sheet.
[readOnly](/css/cssom/styleSheet/readOnly)
:   Non standard. Indicates if the style sheet is currently in read only mode.
[rules](/css/cssom/styleSheet/rules)
:   A collection of rules in a document's stylesheet.
[title](/css/cssom/styleSheet/title)
:   A string used to identify a stylesheet.
[type](/css/cssom/styleSheet/type)
:   The type of a document's stylesheet.

## Methods

API Name
:   Summary
[addPageRule](/css/cssom/methods/addPageRule)
:   Not implemented anywhere. Non standard.
[addImport](/css/cssom/styleSheet/addImport)
:   Non standard. Adds an @import rule to the style sheet.
[blockDirection](/css/cssom/styleSheet/blockDirection)
:
[deleteRule](/css/cssom/styleSheet/deleteRule)
:   Deletes a CSS rule from the style sheet.
[insertRule](/css/cssom/styleSheet/insertRule)
:   Adds a new CSS rule to the stylesheet.
[removeImport](/css/cssom/stylesheet/removeImport)
:   Non standard. Removes an @import rule from the style sheet.
[removeRule](/css/cssom/stylesheet/removeRule)
:   Non standard. Removes a rule from a style sheet.

## Events

*No events.*

## Examples

This example uses the **styleSheet** object to change the cascading style sheets (CSS) values of inline and imported styles.

``` {.html}
<!doctype html>
<html>
 <head>
  <title></title>
  <style>
BODY {background-color: #CFCFCF;}
@import url("otherStyleSheet.css");
  </style>
  <script>
window.onload=fnInit;
function fnInit() {
   // Access a rule in the styleSheet, change backgroundColor to blue.
   var stylesheet = document.styleSheets[0];
   var rule = stylesheet.rules[0];
   rule.style.backgroundColor = "#0000FF";
   // Add a rule for P elements to have yellow backgrounds.
   stylesheet.addRule("P", "background-color: #FFFF00;");
   // Change and imported rule:
   stylesheet.imports[0].color = "#000000";
}
  </script>
 </head>
 <body>
 </body>
</html>
```

## Notes

You can use this object to retrieve style sheet information, such as the URL of the source file for the style sheet and the element in the document that owns (defines) the style sheet. You can also use it to modify style sheets. You can retrieve a **styleSheet** object from the [**styleSheets**](/css/cssom/styleSheets) collection or from the [**imports**](/css/cssom/imports) collection. Each item in these collections is a style sheet. A **styleSheet** object is available for a style sheet only if it is included in a document with a **style** or **link** element, or with an [**@import**](/css/atrules/@import) statement in a **style** element.

#### Non Standard Methods

The **styleSheet** object has these methods.

Method
:   Description
[**addRule**](/css/cssom/methods/addRule)
:   Non standard. Creates a new rule for a style sheet.
[**fireEvent**](/w/index.php?title=dom/methods/fireEvent&action=edit&redlink=1)
:   Fires a specified event on the object.

Â

#### Non Standard Properties

The **styleSheet** object has these properties.

Property
:   Description
[**disabled**](/html/attributes/disabled)
:   Sets or retrieves a value that indicates whether the user can interact with the object.
[**href**](/css/cssom/properties/href)
:   Sets or retrieves the URL of the linked style sheet.
[**id**](/html/attributes/id)
:   Sets or retrieves the string identifying the object.
[**isAlternate**](/css/cssom/properties/isAlternate)
:   Retrieves a value that indicates whether the styleSheet object is an alternative style sheet.
[**isPrefAlternate**](/css/cssom/properties/isPrefAlternate)
:   Retrieves a value that indicates whether the style sheet is the preferred style sheet.
[**media**](/css/cssom/properties/media)
:   Sets or retrieves the media type.
[**ownerNode**](/css/cssom/styleSheet/ownerNode)
:   Retrieves the node that associates this style sheet with the document.
[**parentStyleSheet**](/css/cssom/styleSheet/parentStyleSheet)
:   Retrieves the style sheet that imported the current style sheets.
[**textAutospace**](/css/properties/text-autospace)
:   Sets or retrieves the autospacing and narrow space width adjustment of text.
[**title**](/css/cssom/styleSheet/title)
:   Sets or retrieves the title of the style sheet.
[**type**](/css/cssom/styleSheet/type)
:   Retrieves the CSS language in which the style sheet is written.

Â

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

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

