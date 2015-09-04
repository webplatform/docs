---
title: previousNode
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The NodeIterator.previousNode() method returns the previous node in the set represented by the NodeIterator and moves the position of the iterator backwards within the set.'
uri: dom/NodeIterator/previousNode

---
# previousNode

## Summary

The NodeIterator.previousNode() method returns the previous node in the set represented by the NodeIterator and moves the position of the iterator backwards within the set.

*Method of [dom/NodeIterator](/dom/NodeIterator)*

## Syntax

``` {.js}
var object = object.previousNode(/* see parameter list */);
```

## Parameters

### oNode

 Data-typeÂ
:   any

 Â Object containing the previous node in the list.

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

This method can return one of these values.

Return code
:   Description
S\_OK
:   The operation completed successfully.
InvalidStateError \_ERR
:   NodeIterator raises this exception if detach has been invoked on the object.

Â

This method returns null when the current node is the first node in the set.

[**Node**](/dom/Node)

Â Object containing the previous node in the list.

## Examples

``` {.js}
var nodeIterator = document.createNodeIterator(
    document.body,
    NodeFilter.SHOW_ELEMENT,
    { acceptNode: function(node) { return NodeFilter.FILTER_ACCEPT; } },
    false // this optional argument is not used any more
);
currentNode = nodeIterator.nextNode(); // returns the next node
previousNode = nodeIterator.previousNode(); // same result, since we backtracked to the previous nod
```

## Notes

In old browsers, as specified in old versions of the specifications, the method may throws the INVALID\_STATE\_ERR DOMException if this method is called after the NodeIterator.detach()method. Recent browsers never throw.

### Syntax

node = nodeIterator.previousNode();

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 1.2

## Related specifications

Specification
:   Status
[DOM](http://dom.spec.whatwg.org/#dom-nodeiterator-previousnode)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[NodeIterator.previousNode](https://developer.mozilla.org/en-US/docs/Web/API/NodeIterator.previousNode) Article]

Portions of this content come from the Microsoft Developer Network: [[previousNode Method](http://msdn.microsoft.com/en-us/library/ie/ff975284(v=vs.85).aspx) Article]

