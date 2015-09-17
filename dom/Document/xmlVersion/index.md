---
title: 'xmlVersion'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs compat table'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Document
    href: /dom/Document
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Document
standardization_status: 'W3C Recommendation'
summary: 'Gets or sets the version attribute that is specified in the declaration of an XML document.'
tags:
  - API_Object_Properties
  - DOM
uri: dom/Document/xmlVersion

---
## Summary

Gets or sets the version attribute that is specified in the declaration of an XML document.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
var version = document.xmlVersion;
document.xmlVersion = newVersion;
```

## Return Value

Returns an object of type StringString

The XML **version** of document.

## Examples

The following code example shows an XML declaration that specifies a values for the **version** attribute.

```
<?xml version="1.0"?>
```

## Notes

Applications should use the [**normalize**](/dom/Node/normalize) method after they change the **xmlVersion** property.

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/2004/REC-DOM-Level-3-Core-20040407)
:   Recommendation
