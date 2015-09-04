---
title: error
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'Needs summary, examples, compat, better spec link'
uri: dom/Element/error
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/file/MSStream

---
# error

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Element](/dom/Element)</span></span>

## Syntax

``` {.js}
var result = element.error;
element.error = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

Fires the **onerror** event and passes the associated error to the **error** property. Error codes map directly to World Wide Web Consortium (W3C) file errors, as described in the following table.

Type
:   Description
NotFoundError
:   The resource ([**File**](/apis/file/File), [**Blob**](/apis/file/Blob), or [**msStream**](/w/index.php?title=apis/file/MSStream&action=edit&redlink=1)) could not be found at the time the read was processed.
SecurityError
:   One of the following occurred:
    -   The file being accessed is unsafe.
    -   The file has changed since the user selected it.
    -   Other security issues not covered by other error types.

NotReadableError
:   The resource could not be read. This may occur due to permission problems on the file.
EncodingError
:   The resource could not be encoded due to data URL length limitations.

  This property is `null` unless there is an error.

### Syntax

## See also

### Related pages (MSDN)

-   `FileReader`
-   `msStreamReader`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

