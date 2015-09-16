---
title: 'TreeWalker'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[TreeWalker](https://developer.mozilla.org/en-US/docs/Web/API/TreeWalker) Article]'
  - 'Microsoft Developer Network: [[TreeWalker Object](http://msdn.microsoft.com/en-us/library/ie/ff974360(v=vs.85).aspx) Article]'
notes:
  - "waiting for property and method descriptions to fill description fields... Not sure if all properties and methods have been listed.\nMissing document.createTreeWalker method."
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'Provides an object that can be used to traverse filtered lists of nodes or elements in a document.'
tags:
  - API
  - Objects
  - DOM
uri: dom/TreeWalker

---
## Summary

Provides an object that can be used to traverse filtered lists of nodes or elements in a document.

## Properties

API Name
:   Summary

[currentNode](/dom/TreeWalker/currentNode)
:   Sets or retrieves where the current node in a filtered TreeWalker hierarchy is positioned.

## Methods

API Name
:   Summary

[firstChild](/dom/TreeWalker/firstChild)
:   Retrieves a reference to the first child of the current node of the filtered TreeWalker hierarchy and updates currentNode.

[lastChild](/dom/TreeWalker/lastChild)
:   Retrieves a reference to the last child of the current node of the filtered TreeWalker hierarchy and updates currentNode.

[nextSibling](/dom/TreeWalker/nextSibling)
:   Retrieves the next sibling of the current node in the filtered TreeWalker hierarchy and updates currentNode.

[parentNode](/dom/TreeWalker/parentNode)
:   Retrieves the parent object in the document hierarchy relative to the current node and updates currentNode.

[previousSibling](/dom/TreeWalker/previousSibling)
:   Retrieves the previous sibling of the current node in the filtered TreeWalker hierarchy and updates currentNode.

## Events

*No events.*

## Notes

### Remarks

The **TreeWalker** is dynamic, reflecting the state of the document as it is edited or changed.

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 1.2

## Related specifications

[DOM](http://dom.spec.whatwg.org/#treeWalker)
:   Living Standard
