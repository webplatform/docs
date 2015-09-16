---
title: 'scripts'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, examples, spec, compat'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Document
    href: /dom/Document
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Document/scripts

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
var result = element.scripts;
element.scripts = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

This collection contains all the scripts in the document in source order regardless of the script's location in the document (whether in the **head** or **body**). If duplicate identifiers are found, a collection of those items is returned. Collections of duplicates must be referenced subsequently by ordinal position.

### Standards information

There are no standards that apply here.
