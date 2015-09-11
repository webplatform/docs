---
title: item
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, example, spec reference, standardization status'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/cssom/rules
    href: /css/cssom/rules
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/cssom/rules/item

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [css/cssom/rules](/css/cssom/rules)[css/cssom/rules](/css/cssom/rules)

## <span>Syntax</span>

``` js
var result = element.item;
element.item = value;
```

**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

This function returns an S\_OK even if the element is not found. The programmer should check the value of the *ppHTMLStyleSheetRule* pointer returned by this call. If the value of the pointer is NULL, the element was not found and the call was not successful.

### <span>Parameters</span>

*index* [in]
:   Type: **Integer** ****Integer** that specifies the zero-based index of the object to retrieve.**

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `rules`
