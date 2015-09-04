---
title: removeNamedItem
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
summary: 'Removes an attribute with a given name.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/removeNamedItemEx1.htm'
uri: dom/NamedNodeMap/removeNamedItem

---
# removeNamedItem

## Summary

Removes an attribute with a given name.

*Method of [dom/NamedNodeMap](/dom/NamedNodeMap)*

## Syntax

``` {.js}
var attribute = attributes.removeNamedItem(/* see parameter list */);
```

## Parameters

### name

 Data-typeÂ
:   String

 The name of an [**attribute**](/dom/HTMLElement) to remove.

## Return Value

Returns an object of type DOM Node.

The removed attribute.

## Examples

The following example shows how to use this method to remove an [**attribute**](/dom/HTMLElement) from an element.

``` {.html}
<!doctype html>
<html>
 <head>
<title>removeNamedItem example</title>
  <script>
function removeAttrib() {
    var attributes = document.getElementById("ex").attributes;
    attributes.removeNamedItem("title");
}
  </script>
 </head>
 <body>
 <div onclick="removeAttrib();" id="ex" title="This is a tooltip">
Click this DIV and the tooltip will be deactivated.</div>
 </body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/removeNamedItemEx1.htm)

## Notes

An **attribute** that is removed with this method reverts to the default value of the **attribute** when applicable. This method returns a script error if the user attempts to remove a non-existent attribute node. **removeNamedItem** was introduced in Microsoft Internet ExplorerÂ 6.

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[NamedNodeMap](https://developer.mozilla.org/en-US/docs/Web/API/NamedNodeMap) Article]

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

