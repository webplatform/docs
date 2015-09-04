---
title: result
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
notes:
  - 'Needs summary, examples, specs and compat'
uri: dom/Element/result

---
# result

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Element](/dom/Element)</span></span>

## Syntax

``` {.js}
var result = element.result;
element.result = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The format of the `result` data depends on which of the read methods was used to initiate the read operation. This property can also return partial [**Blob**](/apis/file/Blob) data. Partial **Blob** data is the part of the [**File**](/apis/file/File) or **Blob** that has been read into memory currently; when processing the read method [**readAsText**](/apis/file/FileReader/readAsText), partial **Blob** data is a Document Object Model (DOM) string that is incremented as more bytes are loaded; and when processing [**readAsArrayBuffer**](/apis/file/FileReader/readAsArrayBuffer), partial **Blob** data is an array buffer object consisting of the bytes loaded so far.

### Syntax

## See also

### Related pages (MSDN)

-   `FileReader`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

