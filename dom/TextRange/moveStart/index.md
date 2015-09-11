---
title: moveStart
attributions:
  - 'Microsoft Developer Network: [[moveStart Method](http://msdn.microsoft.com/en-us/library/ie/ms536623(v=vs.85).aspx) Article]'
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
summary: 'Changes the start position of the range.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/TextRange/moveStart

---
## <span>Summary</span>

Changes the start position of the range.

Method of [dom/TextRange](/dom/TextRange)[dom/TextRange](/dom/TextRange)

## <span>Syntax</span>

``` js
var result = textRange.moveStart(/* see parameter list */);
```

## <span>Parameters</span>

### <span>Unit</span>

 Data-type
:   BSTR

**String** that specifies the units to move, using one of the following values:

character - Moves one or more characters.

word - Moves one or more words. A word is a collection of characters terminated by a space or some other white-space character, such as a tab.

sentence - Moves one or more sentences. A sentence is a collection of words terminated by a punctuation character, such as a period.

textedit - Moves to the start or end of the original range.

### <span>Count</span>

 Data-type
:   Number

**Integer** that specifies the number of units to move. This can be positive or negative. The default is **1**.

## <span>Return Value</span>

Returns an object of type NumberNumber

**Integer** that returns the number of units moved.

**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

### <span>Syntax</span>

### <span>Standards information</span>

There are no standards that apply here.