---
title: onload
tags:
  - API
  - Object
  - Properties
readiness: 'Not Ready'
notes:
  - 'Needs summary, examples, spec and compat'
uri: dom/Element/onload

---
# onload

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Element](/dom/Element)</span></span>

## Syntax

``` {.js}
var result = element.onload;
element.onload = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

This event fires when a method finishes the read of a [**Blob**](/apis/file/Blob) object. If the operation fails, **onload** does not fire, but instead, the **onloadend** and **onerror** events fire.

### Syntax

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## See also

### Related pages (MSDN)

-   `FileReader`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

