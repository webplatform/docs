---
title: 'NodeIterator'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[NodeIterator](https://developer.mozilla.org/en-US/docs/Web/API/NodeIterator) Article]'
  - 'Microsoft Developer Network: [[nodeIterator Object](http://msdn.microsoft.com/en-us/library/ie/ff974357(v=vs.85).aspx) Article]'
notes:
  - "missing\ndetach Method"
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'The NodeIterator interface represents an iterator over the members of a list of the nodes in a subtree of the DOM. The nodes will be returned in document order.'
tags:
  - API
  - Objects
  - DOM
uri: dom/NodeIterator

---
## Summary

The NodeIterator interface represents an iterator over the members of a list of the nodes in a subtree of the DOM. The nodes will be returned in document order.

## Properties

API Name
:   Summary

[expandEntityReferences](/dom/NodeIterator/expandEntityReferences)
:   Flag to specify whether or not the children of entity reference nodes are visible.

[filter](/dom/NodeIterator/filter)
:   Gets the currently applied **NodeFilter** to the traversal.

[root](/dom/NodeIterator/root)
:   The NodeIterator.root read-only property represents the Node that is the root of what the NodeIterator traverses.

[whatToShow](/dom/NodeIterator/whatToShow)
:   The NodeIterator.whatToShow read-only property represents an unsigned integer representing a bitmask signifying what types of nodes should be returned by the NodeIterator.

## Methods

API Name
:   Summary

[nextNode](/dom/NodeIterator/nextNode)
:   The NodeIterator.nextNode() method returns the next node in the set represented by the NodeIterator and advances the position of the iterator within the set. The first call to nextNode() returns the first node in the set.

    This method returns null when there are no nodes left in the set.

[previousNode](/dom/NodeIterator/previousNode)
:   The NodeIterator.previousNode() method returns the previous node in the set represented by the NodeIterator and moves the position of the iterator backwards within the set.

## Events

*No events.*

## Examples

``` js
var nodeIterator = document.createNodeIterator(root, whatToShow, filter);
```

## Usage

     Used in web browser Developer Tools UI to provide a consistent and interoperable means of traversing DOM Nodes.

## Notes

### Remarks

The **NodeIterator** is dynamic, reflecting the state of the document as it is edited or changed.

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 1.2
