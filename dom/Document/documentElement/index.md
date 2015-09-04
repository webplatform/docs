---
title: documentElement
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs compat table'
summary: 'Gets the root node of the document.'
uri: dom/Document/documentElement

---
# documentElement

## Summary

Gets the root node of the document.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Document](/dom/Document)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var documentElement = document.documentElement;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">DOM Node</span></span>

The root element of the document.

## Examples

This example uses the **documentElement** property to get the [**innerHTML**](/dom/HTMLElement/innerHTML) property of the entire document, essentially everything inside the `<html>...</html>` tags.

``` {.html}
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

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/core.html#i-Document)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

