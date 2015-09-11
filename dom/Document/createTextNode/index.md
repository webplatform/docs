---
title: createTextNode
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs compat table'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Document
    href: /dom/Document
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Document
standardization_status: 'W3C Recommendation'
summary: 'Creates a text node containing the passed string (nodeValue).'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Document/createTextNode

---
## <span>Summary</span>

Creates a text node containing the passed string (nodeValue).

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## <span>Syntax</span>

``` js
var textNode = document.createTextNode(text);
```

## <span>Parameters</span>

### <span>text</span>

 Data-type
:   String

 The [**nodeValue**](/dom/Node/nodeValue) property of the text node.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

The created TextNode.

## <span>Examples</span>

``` html
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

## <span>Related specifications</span>

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/core.html#ID-1975348127)
:   Recommendation

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `Reference`
-   `createElement`
-   `Conceptual`
-   `About the W3C Document Object Model`
