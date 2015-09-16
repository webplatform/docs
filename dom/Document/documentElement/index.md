---
title: 'documentElement'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs compat table'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Document
    href: /dom/Document
  return:
    predicate: 'Returns an object of type '
    value: 'DOM Node'
    href: /dom/Document
standardization_status: 'W3C Recommendation'
summary: 'Gets the root node of the document.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Document/documentElement

---
## Summary

Gets the root node of the document.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

**Note**: This property is read-only.

``` js
var documentElement = document.documentElement;
```

## Return Value

Returns an object of type DOM NodeDOM Node

The root element of the document.

## Examples

This example uses the **documentElement** property to get the [**innerHTML**](/dom/HTMLElement/innerHTML) property of the entire document, essentially everything inside the `<html>...</html>` tags.

``` html
<!doctype html>
<html>
 <head>
  <script>
function getHTML() {
   var sData = document.documentElement.innerHTML;
   document.getElementById("oResults").value = sData;
}
window.addEventListener("load", getHTML, false);
  </script>
 </head>
 <body>
  <textarea id="oResults" cols="50" rows="10"></textarea>
 </body>
</html>
```

## Notes

The root node of a typical HTML document is the **html** object.

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/core.html#i-Document)
:   Recommendation
