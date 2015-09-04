---
title: xmlVersion
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs compat table'
summary: 'Gets or sets the version attribute that is specified in the declaration of an XML document.'
uri: dom/Document/xmlVersion

---
# xmlVersion

## Summary

Gets or sets the version attribute that is specified in the declaration of an XML document.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Document](/dom/Document)</span></span>

## Syntax

``` {.js}
var version = document.xmlVersion;
document.xmlVersion = newVersion;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The XML **version** of document.

## Examples

The following code example shows an XML declaration that specifies a values for the **version** attribute.

``` {.other}
<?xml version="1.0"?>
```

## Notes

Applications should use the [**normalize**](/dom/Node/normalize) method after they change the **xmlVersion** property.

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/2004/REC-DOM-Level-3-Core-20040407)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

