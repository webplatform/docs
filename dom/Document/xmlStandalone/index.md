---
title: xmlStandalone
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs compat'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Document
    href: /dom/Document
  return:
    predicate: 'Returns an object of type '
    value: Boolean
    href: /dom/Document
standardization_status: 'W3C Recommendation'
summary: 'Gets or sets the value of the standalone attribute in the declaration of an XML document.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Document/xmlStandalone

---
## Summary

Gets or sets the value of the standalone attribute in the declaration of an XML document.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
var isStandalone = document.xmlStandalone;
document.xmlStandalone = isStandalone;
```

## Return Value

Returns an object of type BooleanBoolean

## Examples

The following example shows an XML declaration that specifies a value for the **standalone** attribute.

```
<?xml standalone="yes"?>
```

## Notes

Setting the value of the **xmlStandalone** property does not cause an XML document to validate. Use the [**normalize**](/dom/Node/normalize) method instead.

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/2004/REC-DOM-Level-3-Core-20040407)
:   Recommendation
