---
title: nextSibling
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.nextSibling](https://developer.mozilla.org/en-US/docs/Web/API/Node.nextSibling) Article]'
  - 'Microsoft Developer Network: [[nextSibbling Property](http://msdn.microsoft.com/en-us/library/ie/ms534189(v=vs.85).aspx) Article]'
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
summary: 'Retrieves the next child node of the parent of the node.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Node/nextSibling

---
## Summary

Retrieves the next child node of the parent of the node.

Property of [dom/Node](/dom/Node)[dom/Node](/dom/Node)

## Syntax

**Note**: This property is read-only.

``` js
var nextNode = node.nextSibling;
```

## Return Value

Returns an object of type DOM NodeDOM Node

The next child node of the parent of the node, or null if the node is the last child.

## Examples

This example uses the **nextSibling** property to obtain the next item in the list.

``` html
<body>
<ul id="oList">
<li>List Item 1</li>
<li>List Item 2</li>
<li>List Item 3</li>
</ul>
<script type="text/javascript">
// returns the list item labeled 'List Item 2'
var oSibling = document.getElementById("oList").childNodes(0).nextSibling;
</script>

</body>
```

## Usage

     Used to Enumerate the DOM tree.

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
