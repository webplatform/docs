---
title: empty
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Out of Date'
standardization_status: Non-Standard
notes:
  - "I think the empty method only applies to the selection object, not a node collection.\nthis is legacy MSIE method of document.selection(); and does not apply to document Nodes.\n\nMSDN doco ref: http://msdn.microsoft.com/en-us/library/ie/ms536418(v=vs.85).aspx"
summary: 'Cancels the current selection, sets the selection type to none, and sets the item property to null. '
uri: dom/Node/empty

---
# empty

## Summary

Cancels the current selection, sets the selection type to none, and sets the item property to null.

*Method of [dom/Node](/dom/Node)*

## Syntax

``` {.js}
var result = selection.empty();
```

## Return Value

Returns an object of type Number.

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

**Needs Examples**: This section should include examples.

## See also

### Related pages (MSDN)

-   `Selection`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[empty() Method](http://msdn.microsoft.com/en-us/library/ie/ms536418(v=vs.85).aspx) Article]

