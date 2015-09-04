---
title: serializeToString
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
notes:
  - 'Needs spec reference, standardization status'
summary: 'Converts the parent DOM node of a document tree to an XML string.'
uri: apis/xhr/methods/serializeToString

---
# serializeToString

## Summary

Converts the parent DOM node of a document tree to an XML string.

*Method of [apis/xhr/objects/XMLSerializer](/apis/xhr/objects/XMLSerializer)*

## Syntax

``` {.js}
var object = object.serializeToString(pNode);
```

## Parameters

### pNode

 Data-typeÂ
:   any

 The parent DOM node of a document tree to convert to an XML string.

## Return Value

Returns an object of type DOM Node.

String

The string that contains an XML representation of a DOM node tree.

## Examples

To use the **serializeToString** method, type the following syntax.

``` {.js}
oXmlSerializer =  new XMLSerializer();
sXmlString = oXmlSerializer.serializeToString(oDOMNode);
```

## See also

### Related pages (MSDN)

-   `XMLSerializer`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

