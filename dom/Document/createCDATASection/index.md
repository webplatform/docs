---
title: createCDATASection
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
  - API
  - Object
  - Methods
  - DOM
uri: dom/Document/createCDATASection

---
## <span>Summary</span>

Creates a CDATA section that contains the specified text.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## <span>Syntax</span>

``` js
var cdataSection = document.createCDATASection(text);
```

## <span>Parameters</span>

### <span>text</span>

 Data-type
:   String

 The text to place inside the CDATA section.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

The CDATA section node.

## <span>Examples</span>

The following code example creates a CDATA section.

``` js
document.createCDATASection("My content");
```

## <span>Notes</span>

The **createCDATASection** method is supported only for XML documents.

## <span>Related specifications</span>

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## <span>See also</span>

### <span>Related pages (MSDN)</span>