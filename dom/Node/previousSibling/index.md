---
title: 'previousSibling'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.previousSibling](https://developer.mozilla.org/en-US/docs/Web/API/Node.previousSibling) Article]'
  - 'Microsoft Developer Network: [[previousSibling Property](http://msdn.microsoft.com/en-us/library/ie/ms534350(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Node
    href: /dom/Node
  return:
    predicate: 'Returns an object of type '
    value: 'DOM Node'
    href: /dom/Node
standardization_status: 'W3C Recommendation'
summary: 'Retrieves the previous child node of the parent of the node.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Node/previousSibling

---
## Summary

Retrieves the previous child node of the parent of the node.

Property of [dom/Node](/dom/Node)[dom/Node](/dom/Node)

## Syntax

**Note**: This property is read-only.

``` js
var previousNode = node.previousSibling;
```

## Return Value

Returns an object of type DOM NodeDOM Node

The previous child node of the parent of the node, or null if the node is the first child.

## Examples

This example uses the **previousSibling** property to obtain the previous sibling of a list item.

``` html
<script>
// returns the list item labeled 'List Item 1'
var oSibling = document.getElementById("oList").childNodes[1].previousSibling;
</script>
<body>
 <ul id="oList">
  <li>List Item 1</li>
  <li>List Item 2</li>
  <li>List Item 3</li>
 </ul>
</body>
```

## Related specifications

[DOM Level 1](http://www.w3.org/TR/REC-DOM-Level-1/)
:   Recommendation
