---
title: moveToElementText
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
  - API
  - Object
  - Methods
  - DOM
uri: dom/TextRange/moveToElementText

---
## <span>Summary</span>

Moves the text range so that the start and end positions of the range encompass the text in the given element.

Method of [dom/TextRange](/dom/TextRange)[dom/TextRange](/dom/TextRange)

## <span>Syntax</span>

``` js
var result = textRange.moveToElementText(/* see parameter list */);
```

## <span>Parameters</span>

### <span>element</span>

 Data-type
:   any

**Object** that specifies the element object to move to.

## <span>Return Value</span>

Returns an object of type NumberNumber

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>