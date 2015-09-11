---
title: adoptNode
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
  - API
  - Object
  - Methods
  - DOM
uri: dom/Document/adoptNode

---
## <span>Summary</span>

Tries to move a node from one document to the document that the document object displays. It is preferable to use importNode instead.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## <span>Syntax</span>

``` js
var element = document.adoptNode(/* see parameter list */);
```

## <span>Parameters</span>

### <span>element</span>

 Data-type
:   DOM Node

 The element to move.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

The node that has been moved, or a null value if the node cannot be moved.

## <span>Examples</span>

The following code example illustrates the **adoptNode** method and shows one way to handle cases where the method fails.

``` js
var oNode = document.adoptNode( oXHTMLNode );
if ( oNode == null )
   oNode = document.importNode( oXHTMLNode );
parent.appendChild( oNode );
```

## <span>Related specifications</span>

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
