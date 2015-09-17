---
title: 'empty'
attributions:
  - 'Microsoft Developer Network: [[empty() Method](http://msdn.microsoft.com/en-us/library/ie/ms536418(v=vs.85).aspx) Article]'
notes:
  - "I think the empty method only applies to the selection object, not a node collection.\nthis is legacy MSIE method of document.selection(); and does not apply to document Nodes.\n\nMSDN doco ref: http://msdn.microsoft.com/en-us/library/ie/ms536418(v=vs.85).aspx"
readiness: 'Out of Date'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Node
    href: /dom/Node
  return_type:
    predicate: 'Returns an object of type  '
    value: Number
    href: /dom/Node
standardization_status: Non-Standard
summary: 'Cancels the current selection, sets the selection type to none, and sets the item property to null. '
tags:
  - API_Object_Methods
  - DOM
  - Needs_Examples
uri: dom/Node/empty

---
## Summary

Cancels the current selection, sets the selection type to none, and sets the item property to null.

Method of [dom/Node](/dom/Node)[dom/Node](/dom/Node)

## Syntax

``` js
var result = selection.empty();
```

## Return Value

Returns an object of type NumberNumber

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## See also

### Related pages

-   Selection[Selection](/dom/Selection)
