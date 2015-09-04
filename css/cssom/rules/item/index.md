---
title: item
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
notes:
  - 'Needs summary, example, spec reference, standardization status'
uri: css/cssom/rules/item

---
# item

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/cssom/rules](/css/cssom/rules)</span></span>

## Syntax

``` {.js}
var result = element.item;
element.item = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

This function returns an S\_OK even if the element is not found. The programmer should check the value of the *ppHTMLStyleSheetRule* pointer returned by this call. If the value of the pointer is NULL, the element was not found and the call was not successful.

### Parameters

*index* [in]
:   Type: **Integer** ****Integer** that specifies the zero-based index of the object to retrieve.**

## See also

### Related pages (MSDN)

-   `rules`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

