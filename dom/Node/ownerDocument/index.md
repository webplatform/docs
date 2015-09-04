---
title: ownerDocument
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Retrieves the document object associated with the node.'
uri: dom/Node/ownerDocument

---
# ownerDocument

## Summary

Retrieves the document object associated with the node.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Node](/dom/Node)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var doc = element.ownerDocument;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">DOM Node</span></span>

The document Node of the web page or iframe or frame.

The document object returned by this property is the main object with which all the child nodes in the actual HTML document are created. If this property is used on a node that is itself a document, the result is null.

## Examples

    // given a node "p", get the top-level HTML child
    // of the document object

    var doc = p.ownerDocument;
    alert(doc.outerHTML);
    var html = doc.documentElement;
    alert(html.outerHTML);

## Usage

     Used to build the DOM tree of documents that contain <iframe>, <frame> and <frameset> elements.

## Notes

### Remarks

The **ownerDocument** is the [Document](/dom/Document) object that is used to create new nodes. This property returns null when the node is a [Document](/dom/Document). **ownerDocument** was introduced in Microsoft Internet Explorer 6.

### Syntax

var doc=element.ownerDocument;

## Related specifications

Specification
:   Status
[DOM Level 2 Core](http://www.w3.org/TR/2000/REC-DOM-Level-2-Core-20001113/core.html#node-ownerDoc)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.ownerDocument](https://developer.mozilla.org/en-US/docs/Web/API/Node.ownerDocument) Article]

Portions of this content come from the Microsoft Developer Network: [[ownerDocument Property](http://msdn.microsoft.com/en-us/library/ie/ms534315(v=vs.85).aspx) Article]

