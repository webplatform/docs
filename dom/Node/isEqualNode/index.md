---
title: 'isEqualNode'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.isEqual](https://developer.mozilla.org/en-US/docs/Web/API/Node.isEqualNode) Article]'
  - 'Microsoft Developer Network: [[isEqualNode Method](http://msdn.microsoft.com/en-us/library/ie/ff975128(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Node
    href: /dom/Node
  return_type:
    predicate: 'Returns an object of type  '
    value: Boolean
    href: /dom/Node
standardization_status: 'W3C Recommendation'
summary: 'Determines whether two nodes are equal in their type, name and namespace.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/Node/isEqualNode

---
## Summary

Determines whether two nodes are equal in their type, name and namespace.

Method of [dom/Node](/dom/Node)[dom/Node](/dom/Node)

## Syntax

``` js
var isEqual = node.isEqualNode(/* see parameter list */);
```

## Parameters

### otherNode

 Data-type
:   DOM Node

 The node to be compared to the node that is executing the method.

## Return Value

Returns an object of type BooleanBoolean

Whether the node specified in the *otherNode* parameter is equal to the current node.

## Examples

In the follow example if \#targetElm is the first div element of the document 'true' will be displayed.

``` html
var targetElm = document.getElementById("targetElm");
var firstDiv = document.getElementsByTagName("div")[0];

alert( targetElm.isEqualNode(firstDiv) );
```

## Usage

     This method determines whether or not two nodes are equal.  Nodes are considered equal when the values of the following attributes are equal:

-   [**nodeType**](/dom/Node/nodeType)
-   [**nodeName**](/dom/Node/nodeName)
-   [**localName**](/dom/Node/localName)
-   [**namespaceURI**](/dom/Node/namespaceURI)

## Notes

Nodes can be equal without being the same. Use [**isSameNode**](/dom/Node/isSameNode) to determine if two nodes are the same.

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
