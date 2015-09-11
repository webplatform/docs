---
title: xmlEncoding
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
    value: String
    href: /dom/Document
standardization_status: 'W3C Recommendation'
summary: 'Gets a value that represents the character encoding that is specified in the declaration of an XML document.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Document/xmlEncoding

---
## <span>Summary</span>

Gets a value that represents the character encoding that is specified in the declaration of an XML document.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var encoding = document.xmlEncoding;
```

## <span>Return Value</span>

Returns an object of type StringString

The encoding name that is specified in the declaration of an XML document.

## <span>Examples</span>

The following code example shows an XML declaration that specifies character encoding.

```
<?xml encoding="UTF-8"?>
```

## <span>Related specifications</span>

[DOM Level 3 Core](http://www.w3.org/TR/2004/REC-DOM-Level-3-Core-20040407)
:   Recommendation
