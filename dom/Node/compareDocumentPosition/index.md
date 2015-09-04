---
title: compareDocumentPosition
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Compares the position of two nodes in a document.'
uri: dom/Node/compareDocumentPosition

---
# compareDocumentPosition

## Summary

Compares the position of two nodes in a document.

*Method of [dom/Node](/dom/Node)*

## Syntax

``` {.js}
var positionBitmask = node.compareDocumentPosition(/* see parameter list */);
```

## Parameters

### otherNode

 Data-typeÂ
:   DOM Node

 The node to be compared to the reference node, which is the node executing the method.

## Return Value

Returns an object of type Number.

Describes how the position of the node specified by the *otherNode* parameter relates to the position of the reference node. The return value contains one or more of the following flag values:

[Node](/dom/Node) constant name
:   Return value (Integer)
DOCUMENT\_POSITION\_DISCONNECTED
:   1
DOCUMENT\_POSITION\_PRECEDING
:   2
DOCUMENT\_POSITION\_FOLLOWING
:   4
DOCUMENT\_POSITION\_CONTAINS
:   8
DOCUMENT\_POSITION\_CONTAINED\_BY
:   16
DOCUMENT\_POSITION\_IMPLEMENTATION\_SPECIFIC
:   32

Â

## Examples

This example determines if the web document is incorrectly marked up with the body element before the head element. Note: Web browsers sometimes self correct markup errors. HTML5 is the first specification to give guidelines to browser vendors on how they should correct markup errors.

``` {.html}
var head = document.getElementsByTagName('head').item(0);
if (head.compareDocumentPosition(document.body) & Node.DOCUMENT_POSITION_FOLLOWING) {
  console.log("well-formed document");
} else {
  console.log("<head> is not before <body>");
}
```

## Notes

For information about the factors that affect the position of nodes within the DOM, see the related specifications.

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.compareDocumentPosition](https://developer.mozilla.org/en-US/docs/Web/API/Node.compareDocumentPosition) Article]

Portions of this content come from the Microsoft Developer Network: [[compareDocumentPosition Method](http://msdn.microsoft.com/en-us/library/ie/ff975125(v=vs.85).aspx) Article]

