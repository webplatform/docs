---
title: previousSibling
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Retrieves the previous child node of the parent of the node.'
uri: dom/Node/previousSibling

---
# previousSibling

## Summary

Retrieves the previous child node of the parent of the node.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Node](/dom/Node)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var previousNode = node.previousSibling;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">DOM Node</span></span>

The previous child node of the parent of the node, or null if the node is the first child.

## Examples

This example uses the **previousSibling** property to obtain the previous sibling of a list item.

``` {.html}
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

Specification
:   Status
[DOM Level 1](http://www.w3.org/TR/REC-DOM-Level-1/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.previousSibling](https://developer.mozilla.org/en-US/docs/Web/API/Node.previousSibling) Article]

Portions of this content come from the Microsoft Developer Network: [[previousSibling Property](http://msdn.microsoft.com/en-us/library/ie/ms534350(v=vs.85).aspx) Article]

