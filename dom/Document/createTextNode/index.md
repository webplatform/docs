---
title: createTextNode
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs compat table'
summary: 'Creates a text node containing the passed string (nodeValue).'
uri: dom/Document/createTextNode

---
# createTextNode

## Summary

Creates a text node containing the passed string (nodeValue).

*Method of [dom/Document](/dom/Document)*

## Syntax

``` {.js}
var textNode = document.createTextNode(text);
```

## Parameters

### text

 Data-typeÂ
:   String

 The [**nodeValue**](/dom/Node/nodeValue) property of the text node.

## Return Value

Returns an object of type DOM Node.

The created TextNode.

## Examples

``` {.html}
<script>
//create a text node and replace an existing node with the new one
function changeNode() {
   var textNode = document.createTextNode("New Text");
   var replaceNode = document.getElementById("span").childNodes(0);
   replaceNode.replaceNode(textNode);
}
</script>
<span id="span" onclick="changeNode()">
Original Text
</span>
```

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/core.html#ID-1975348127)
:   Recommendation

## See also

### Related pages (MSDN)

-   `Reference`
-   `createElement`
-   `Conceptual`
-   `About the W3C Document Object Model`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

