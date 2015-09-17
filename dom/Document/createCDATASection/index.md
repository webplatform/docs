---
title: 'createCDATASection'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs compat table'
readiness: 'Almost Ready'
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
summary: 'Creates a CDATA section  that contains the specified text.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/Document/createCDATASection

---
## Summary

Creates a CDATA section that contains the specified text.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
var cdataSection = document.createCDATASection(text);
```

## Parameters

### text

 Data-type
:   String

 The text to place inside the CDATA section.

## Return Value

Returns an object of type DOM NodeDOM Node

The CDATA section node.

## Examples

The following code example creates a CDATA section.

``` js
document.createCDATASection("My content");
```

## Notes

The **createCDATASection** method is supported only for XML documents.

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## See also

### Related pages
