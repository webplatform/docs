---
title: createAttributeNS
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Document
    href: /dom/Document
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Document
standardization_status: 'W3C Recommendation'
summary: 'Creates a reference to an attribute object that is associated with an XML namespace.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Document/createAttributeNS

---
## Summary

Creates a reference to an attribute object that is associated with an XML namespace.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
var attribute = document.createAttributeNS(namespace, name);
```

## Parameters

### namespace

 Data-type
:   String

 The name of the desired namespace or a null value if no namespace is desired.

### name

 Data-type
:   String

 The name of the desired attribute.

## Return Value

Returns an object of type DOM NodeDOM Node

The created attribute.

## Examples

``` js
//create a "lang" attribute associated with a namespace
var attr = document.createAttributeNS("http://www.w3.org/XML/1998/namespace", "xml:lang");
//assign a value to the attribute
attr.nodeValue = "es-us";
//apply the attribute to the documentElement (e.g., the XML document's root node)
document.documentElement.setAttributeNodeNS(attr);
```

## Notes

**createAttributeNS** is an XML DOM method and is supported only for XML documents.

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## See also

### Related pages

-   `createAttribute`
