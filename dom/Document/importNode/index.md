---
title: importNode
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'Needs compat tables'
summary: 'Imports a node from another document into the the document that the document object displays.'
uri: dom/Document/importNode

---
# importNode

## Summary

Imports a node from another document into the the document that the document object displays.

*Method of [dom/Document](/dom/Document)*

## Syntax

``` {.js}
var importedNode = document.importNode(node, deep);
```

## Parameters

### node

 Data-typeÂ
:   DOM Node

 The node to import.

### deep

 Data-typeÂ
:   Boolean

*(Optional)*

Whether child nodes of the node specified by the *node* parameter are also imported.

## Return Value

Returns an object of type DOM Node.

The node node that has been imported, or a null if the node cannot be imported.

## Examples

The following code example illustrates the **importNode** method.

``` {.js}
var oNode = document.importNode( oXHTMLNode, false);
parent.appendChild( oNode );
```

## Related specifications

Specification
:   Status
[DOM Level 4](http://www.w3.org/TR/2014/CR-dom-20140508/#dom-document-importnode)
:   Candidate Recommendation
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

