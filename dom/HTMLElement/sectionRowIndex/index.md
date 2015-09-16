---
title: 'sectionRowIndex'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, examples, clean-up of MSDN import'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLElement/sectionRowIndex

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var result = element.sectionRowIndex;
element.sectionRowIndex = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The **tBody**, **tHead**, and **tFoot** sections are mutually exclusive, so a **tr** is always contained in one of these sections and in the [**table**](/html/elements/table). The [**rowIndex**](/dom/HTMLElement/rowIndex) property indicates the position of the object in the [**rows**](/dom/HTMLElement/rows) collection for the **table**. Collection indexes are in source order of the HTML document.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5
