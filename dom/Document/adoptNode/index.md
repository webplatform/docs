---
title: 'adoptNode'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Deprecated; deletion candidate'
readiness: 'Not Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Document
    href: /dom/Document
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Document
standardization_status: Deprecated
summary: 'Tries to move a node from one document to the document that the document object displays. It is preferable to use importNode instead.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/Document/adoptNode

---
## Summary

Tries to move a node from one document to the document that the document object displays. It is preferable to use importNode instead.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
var element = document.adoptNode(/* see parameter list */);
```

## Parameters

### element

 Data-type
:   DOM Node

 The element to move.

## Return Value

Returns an object of type DOM NodeDOM Node

The node that has been moved, or a null value if the node cannot be moved.

## Examples

The following code example illustrates the **adoptNode** method and shows one way to handle cases where the method fails.

``` js
var oNode = document.adoptNode( oXHTMLNode );
if ( oNode == null )
   oNode = document.importNode( oXHTMLNode );
parent.appendChild( oNode );
```

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
