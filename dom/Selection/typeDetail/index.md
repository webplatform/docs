---
title: typeDetail
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Out of Date'
notes:
  - "Not in the spec or MSDN/MDN documentation\nPlease delete"
uri: dom/Selection/typeDetail

---
# typeDetail

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Selection](/dom/Selection)</span></span>

## Syntax

``` {.js}
var result = element.typeDetail;
element.typeDetail = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The default implementation of this property returns a value of `undefined`. Host applications can provide a custom selection mechanism and can provide a value for this property that indicates the selection type. *MSHTML* requests the selection type from the host application by calling **GetTypeDetail**.

### Syntax

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

