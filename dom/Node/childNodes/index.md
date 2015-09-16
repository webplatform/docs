---
title: childNodes
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.childNodes](https://developer.mozilla.org/en-US/docs/Web/API/Node.childNodes) Article]'
  - 'Microsoft Developer Network: [[childNodes Property](http://msdn.microsoft.com/en-us/library/ie/ms537445(v=vs.85).aspx) Article]'
notes:
  - 'Needs some more content.'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Node
    href: /dom/Node
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /dom/Node
standardization_status: 'W3C Recommendation'
summary: 'Gets a collection of direct Node descendants of the Node, including Element, Text and any other type of nodes.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Node/childNodes

---
## Summary

Gets a collection of direct Node descendants of the Node, including Element, Text and any other type of nodes.

Property of [dom/Node](/dom/Node)[dom/Node](/dom/Node)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.childNodes;
```

## Return Value

Returns an object of type

A live collection of the direct Node descendants of the Node.

## Examples

This example shows how to assign to a variable the **childNodes** collection of the **body** object.

``` html
<script>
var aNodeList = oBody.childNodes;
</script>
<body id="oBody">
<span id="oSpan">A Span</span>
</body>
```

This example shows how to assign to a variable the **childNodes** collection of a node created with the [**createElement**](/dom/Document/createElement) method.

``` js
var oParentNode = document.createElement("DIV");
var oNode = document.createElement("B");
document.body.insertBefore(oParentNode);
oParentNode.insertBefore(oNode);
var aNodeList = oParentNode.childNodes;
```

## Notes

The **childNodes** collection can contain [**Element**](/dom/Element) and [**Text**](/dom/Text) nodes. If you check the **childNodes** collection of an element created through standard HTML, you encounter [**Text**](/dom/Text) nodes in unexpected places—in place of line breaks, for example. Alternately, if you create an element using the Document Object Model (DOM), no unintended [**Text**](/dom/Text) nodes are created.
