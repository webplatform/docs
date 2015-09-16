---
title: 'item'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/cssom/pages
    href: /css/cssom/pages
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/cssom/pages/item

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [css/cssom/pages](/css/cssom/pages)[css/cssom/pages](/css/cssom/pages)

## Syntax

``` js
var result = element.item;
element.item = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

This function returns S\_OK even if the element is not found. The programmer should check the value of the *ppHTMLStyleSheetPage* pointer returned by this call. If the value of the pointer is null, the element was not found and the call was not successful.

### Syntax

### Standards information

There are no standards that apply here.

### Parameters

*index* [in]
:   Type: **Integer** ****Integer** that specifies the zero-based index of the object to retrieve.**

## See also

### Related pages

-   pages[pages](/css/cssom/pages)
