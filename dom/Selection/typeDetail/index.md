---
title: typeDetail
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - "Not in the spec or MSDN/MDN documentation\nPlease delete"
readiness: 'Out of Date'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Selection
    href: /dom/Selection
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Selection/typeDetail

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/Selection](/dom/Selection)[dom/Selection](/dom/Selection)

## Syntax

``` js
var result = element.typeDetail;
element.typeDetail = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The default implementation of this property returns a value of `undefined`. Host applications can provide a custom selection mechanism and can provide a value for this property that indicates the selection type. *MSHTML* requests the selection type from the host application by calling **GetTypeDetail**.

### Syntax
