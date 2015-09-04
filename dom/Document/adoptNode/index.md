---
title: adoptNode
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Not Ready'
standardization_status: Deprecated
notes:
  - 'Deprecated; deletion candidate'
summary: 'Tries to move a node from one document to the document that the document object displays. It is preferable to use importNode instead.'
uri: dom/Document/adoptNode

---
# adoptNode

## Summary

Tries to move a node from one document to the document that the document object displays. It is preferable to use importNode instead.

*Method of [dom/Document](/dom/Document)*

## Syntax

``` {.js}
var element = document.adoptNode(/* see parameter list */);
```

## Parameters

### element

 Data-typeÂ
:   DOM Node

 The element to move.

## Return Value

Returns an object of type DOM Node.

The node that has been moved, or a null value if the node cannot be moved.

## Examples

The following code example illustrates the **adoptNode** method and shows one way to handle cases where the method fails.

``` {.js}
var oNode = document.adoptNode( oXHTMLNode );
if ( oNode == null )
   oNode = document.importNode( oXHTMLNode );
parent.appendChild( oNode );
```

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

