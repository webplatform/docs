---
title: xmlStandalone
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs compat'
summary: 'Gets or sets the value of the standalone attribute in the declaration of an XML document.'
uri: dom/Document/xmlStandalone

---
# xmlStandalone

## Summary

Gets or sets the value of the standalone attribute in the declaration of an XML document.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Document](/dom/Document)</span></span>

## Syntax

``` {.js}
var isStandalone = document.xmlStandalone;
document.xmlStandalone = isStandalone;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

## Examples

The following example shows an XML declaration that specifies a value for the **standalone** attribute.

``` {.other}
<?xml standalone="yes"?>
```

## Notes

Setting the value of the **xmlStandalone** property does not cause an XML document to validate. Use the [**normalize**](/dom/Node/normalize) method instead.

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/2004/REC-DOM-Level-3-Core-20040407)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

