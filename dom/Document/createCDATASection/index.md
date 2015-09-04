---
title: createCDATASection
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs compat table'
summary: 'Creates a CDATA section  that contains the specified text.'
uri: dom/Document/createCDATASection

---
# createCDATASection

## Summary

Creates a CDATA section that contains the specified text.

*Method of [dom/Document](/dom/Document)*

## Syntax

``` {.js}
var cdataSection = document.createCDATASection(text);
```

## Parameters

### text

 Data-typeÂ
:   String

 The text to place inside the CDATA section.

## Return Value

Returns an object of type DOM Node.

The CDATA section node.

## Examples

The following code example creates a CDATA section.

``` {.js}
document.createCDATASection("My content");
```

## Notes

The **createCDATASection** method is supported only for XML documents.

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## See also

### Related pages (MSDN)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

