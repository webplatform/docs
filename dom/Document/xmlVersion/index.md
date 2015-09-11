---
title: xmlVersion
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
  - API
  - Object
  - Properties
  - DOM
uri: dom/Document/xmlVersion

---
## <span>Summary</span>

Gets or sets the version attribute that is specified in the declaration of an XML document.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## <span>Syntax</span>

``` js
var version = document.xmlVersion;
document.xmlVersion = newVersion;
```

## <span>Return Value</span>

Returns an object of type StringString

The XML **version** of document.

## <span>Examples</span>

The following code example shows an XML declaration that specifies a values for the **version** attribute.

```
<?xml version="1.0"?>
```

## <span>Notes</span>

Applications should use the [**normalize**](/dom/Node/normalize) method after they change the **xmlVersion** property.

## <span>Related specifications</span>

[DOM Level 3 Core](http://www.w3.org/TR/2004/REC-DOM-Level-3-Core-20040407)
:   Recommendation
