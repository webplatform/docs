---
title: ownerDocument
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.ownerDocument](https://developer.mozilla.org/en-US/docs/Web/API/Node.ownerDocument) Article]'
  - 'Microsoft Developer Network: [[ownerDocument Property](http://msdn.microsoft.com/en-us/library/ie/ms534315(v=vs.85).aspx) Article]'
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
summary: 'Retrieves the document object associated with the node.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Node/ownerDocument

---
## Summary

Retrieves the document object associated with the node.

Property of [dom/Node](/dom/Node)[dom/Node](/dom/Node)

## Syntax

**Note**: This property is read-only.

``` js
var doc = element.ownerDocument;
```

## Return Value

Returns an object of type DOM NodeDOM Node

The document Node of the web page or iframe or frame.

The document object returned by this property is the main object with which all the child nodes in the actual HTML document are created. If this property is used on a node that is itself a document, the result is null.

## Examples

``` html
// given a node "p", get the top-level HTML child
// of the document object

var doc = p.ownerDocument;
alert(doc.outerHTML);
var html = doc.documentElement;
alert(html.outerHTML);
```

## Usage

     Used to build the DOM tree of documents that contain <iframe>, <frame> and <frameset> elements.

## Notes

### Remarks

The **ownerDocument** is the [Document](/dom/Document) object that is used to create new nodes. This property returns null when the node is a [Document](/dom/Document). **ownerDocument** was introduced in Microsoft Internet Explorer 6.

### Syntax

var doc=element.ownerDocument;

## Related specifications

[DOM Level 2 Core](http://www.w3.org/TR/2000/REC-DOM-Level-2-Core-20001113/core.html#node-ownerDoc)
:   Recommendation
