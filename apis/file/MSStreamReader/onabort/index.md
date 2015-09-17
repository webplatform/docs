---
title: 'onabort'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Non-standard; deletion candidate'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/file/MSStreamReader
    href: /apis/file/MSStreamReader
standardization_status: Non-Standard
summary: 'Indicates that the read has been aborted (for example, by calling abort()).'
tags:
  - API_Object_Properties
  - API
  - FileAPI
  - Needs_Examples
  - Deletion_Candidate
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/file/methods/abort
    - dom/methods/click
uri: apis/file/MSStreamReader/onabort

---
## Summary

Indicates that the read has been aborted (for example, by calling abort()).

Property of [apis/file/MSStreamReader](/apis/file/MSStreamReader)[apis/file/MSStreamReader](/apis/file/MSStreamReader)

## Syntax

``` js
var result = element.onabort;
element.onabort = value;
```

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

### Related pages

-   FileReader[FileReader](/apis/file/FileReader)
-   msStreamReader[msStreamReader](/apis/file/MSStreamReader)
-   click[click](/w/index.php?title=dom/methods/click&action=edit&redlink=1)

