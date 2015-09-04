---
title: isEqualNode
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Determines whether two nodes are equal in their type, name and namespace.'
uri: dom/Node/isEqualNode

---
# isEqualNode

## Summary

Determines whether two nodes are equal in their type, name and namespace.

*Method of [dom/Node](/dom/Node)*

## Syntax

``` {.js}
var isEqual = node.isEqualNode(/* see parameter list */);
```

## Parameters

### otherNode

 Data-typeÂ
:   DOM Node

 The node to be compared to the node that is executing the method.

## Return Value

Returns an object of type Boolean.

Whether the node specified in the *otherNode* parameter is equal to the current node.

## Examples

In the follow example if \#targetElm is the first div element of the document 'true' will be displayed.

    var targetElm = document.getElementById("targetElm");
    var firstDiv = document.getElementsByTagName("div")[0];

    alert( targetElm.isEqualNode(firstDiv) );

## Usage

     This method determines whether or not two nodes are equal.  Nodes are considered equal when the values of the following attributes are equal:

-   [**nodeType**](/dom/Node/nodeType)
-   [**nodeName**](/dom/Node/nodeName)
-   [**localName**](/dom/Node/localName)
-   [**namespaceURI**](/dom/Node/namespaceURI)

## Notes

Nodes can be equal without being the same. Use [**isSameNode**](/dom/Node/isSameNode) to determine if two nodes are the same.

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.isEqual](https://developer.mozilla.org/en-US/docs/Web/API/Node.isEqualNode) Article]

Portions of this content come from the Microsoft Developer Network: [[isEqualNode Method](http://msdn.microsoft.com/en-us/library/ie/ff975128(v=vs.85).aspx) Article]

