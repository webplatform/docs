---
title: onabort
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
  0: API
  1: Object
  2: Properties
  4: FileAPI
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/file/methods/abort
    - dom/methods/click
uri: apis/file/MSStreamReader/onabort

---
## <span>Summary</span>

Indicates that the read has been aborted (for example, by calling abort()).

Property of [apis/file/MSStreamReader](/apis/file/MSStreamReader)[apis/file/MSStreamReader](/apis/file/MSStreamReader)

## <span>Syntax</span>

``` js
var result = element.onabort;
element.onabort = value;
```

**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

Aborts a read by, or a creation of, an [**msStreamReader**](/apis/file/MSStreamReader) object. To invoke this event, do one of the following:

-   Abort the creation of an [**msStreamReader**](/apis/file/MSStreamReader) object.
-   Invoke the [**abort**](/w/index.php?title=apis/file/methods/abort&action=edit&redlink=1) method.

The *pEvtObj* parameter is required for the following interfaces:

-   [**msStreamReader**](/apis/file/MSStreamReader)

### <span>Syntax</span>

### <span>Event handler parameters</span>

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `FileReader`
-   `msStreamReader`
-   `click`

**Deletion Candidate**: MS proprietary

