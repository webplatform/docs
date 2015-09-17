---
title: 'moveToElementText'
attributions:
  - 'Microsoft Developer Network: [[moveToElementText Method](http://msdn.microsoft.com/en-us/library/ie/ms536630(v=vs.85).aspx) Article]'
notes:
  - 'needs example'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/TextRange
    href: /dom/TextRange
  return_type:
    predicate: 'Returns an object of type  '
    value: Number
    href: /dom/TextRange
standardization_status: Non-Standard
summary: 'Moves the text range so that the start and end positions of the range encompass the text in the given element.'
tags:
  - API_Object_Methods
  - DOM
  - Needs_Examples
uri: dom/TextRange/moveToElementText

---
## Summary

Moves the text range so that the start and end positions of the range encompass the text in the given element.

Method of [dom/TextRange](/dom/TextRange)[dom/TextRange](/dom/TextRange)

## Syntax

``` js
var result = textRange.moveToElementText(/* see parameter list */);
```

## Parameters

### element

 Data-type
:   any

**Object** that specifies the element object to move to.

## Return Value

Returns an object of type NumberNumber

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Notes

### Remarks
