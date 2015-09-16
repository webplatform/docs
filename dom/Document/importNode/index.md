---
title: 'importNode'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs compat tables'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Document
    href: /dom/Document
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Document
standardization_status: 'W3C Candidate Recommendation'
summary: 'Imports a node from another document into the the document that the document object displays.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Document/importNode

---
## Summary

Imports a node from another document into the the document that the document object displays.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
var importedNode = document.importNode(node, deep);
```

## Parameters

### node

 Data-type
:   DOM Node

 The node to import.

### deep

 Data-type
:   Boolean

(Optional)

Whether child nodes of the node specified by the *node* parameter are also imported.

## Return Value

Returns an object of type DOM NodeDOM Node

The node node that has been imported, or a null if the node cannot be imported.

## Examples

The following code example illustrates the **importNode** method.

``` js
var oNode = document.importNode( oXHTMLNode, false);
parent.appendChild( oNode );
```

## Related specifications

[DOM Level 4](http://www.w3.org/TR/2014/CR-dom-20140508/#dom-document-importnode)
:   Candidate Recommendation

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
