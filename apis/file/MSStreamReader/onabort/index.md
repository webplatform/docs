---
title: onabort
tags:
  0: API
  1: Object
  2: Properties
  4: FileAPI
readiness: 'Not Ready'
standardization_status: Non-Standard
notes:
  - 'Non-standard; deletion candidate'
summary: 'Indicates that the read has been aborted (for example, by calling abort()).'
uri: apis/file/MSStreamReader/onabort
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/file/methods/abort
    - dom/methods/click

---
# onabort

## Summary

Indicates that the read has been aborted (for example, by calling abort()).

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/file/MSStreamReader](/apis/file/MSStreamReader)</span></span>

## Syntax

``` {.js}
var result = element.onabort;
element.onabort = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

Aborts a read by, or a creation of, an [**msStreamReader**](/apis/file/MSStreamReader) object. To invoke this event, do one of the following:

-   Abort the creation of an [**msStreamReader**](/apis/file/MSStreamReader) object.
-   Invoke the [**abort**](/w/index.php?title=apis/file/methods/abort&action=edit&redlink=1) method.

The *pEvtObj* parameter is required for the following interfaces:

-   [**msStreamReader**](/apis/file/MSStreamReader)

### Syntax

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## See also

### Related pages (MSDN)

-   `FileReader`
-   `msStreamReader`
-   `click`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

**Deletion Candidate**: MS proprietary

