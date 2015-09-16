---
title: insertNode
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.insertNode](https://developer.mozilla.org/en-US/docs/Web/API/Range.insertNode) Article]'
  - 'Microsoft Developer Network: [[insertNode Method](http://msdn.microsoft.com/en-us/library/ie/ff975445(v=vs.85).aspx) Article]'
notes:
  - 'Needs some more content.'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Range
    href: /dom/Range
standardization_status: 'W3C Recommendation'
summary: 'Inserts a Node into the start of a Range object.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Range/insertNode

---
## Summary

Inserts a Node into the start of a Range object.

Method of [dom/Range](/dom/Range)[dom/Range](/dom/Range)

## Syntax

``` js
 newNode.insertNode(/* see parameter list */);
```

## Parameters

### oNode

 Data-type
:   DOM Node

 The new node to insert.

## Return Value

No return value

## Examples

``` js
var range = document.createRange();
newNode = document.createElement("p");
newNode.appendChild(document.createTextNode("New Node Inserted Here"));
range.selectNode(document.getElementsByTagName("div").item(0));
range.insertNode(newNode);
```

## Notes

If the container is a node of type [**Text**](/dom/Text), **insertNode** splits the text node, and inserts *newNode* between the resulting two text nodes. If *newNode* is a document fragment, the children of the document fragment node are inserted rather than the *newNode* itself.

## Related specifications

[DOM](http://dom.spec.whatwg.org/#dom-range-insertnode)
:   Living Standard

[Document Object Model (DOM) Level 2 Traversal and Range](http://www.w3.org/TR/DOM-Level-2-Traversal-Range/ranges.html#Level2-Range-method-insertNode)
:   W3C Recommendation
