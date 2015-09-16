---
title: moveEnd
attributions:
  - 'Microsoft Developer Network: [[moveEnd Method](http://msdn.microsoft.com/en-us/library/ie/ms536620(v=vs.85).aspx) Article]'
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
summary: 'Changes the end position of the range.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/TextRange/moveEnd

---
## Summary

Changes the end position of the range.

Method of [dom/TextRange](/dom/TextRange)[dom/TextRange](/dom/TextRange)

## Syntax

``` js
var result = textRange.moveEnd(/* see parameter list */);
```

## Parameters

### Unit

 Data-type
:   BSTR

**String** that specifies the units to move, using one of the following values:

character - Moves one or more characters.

word - Moves one or more words. A word is a collection of characters terminated by a space or some other white-space character, such as a tab.

sentence - Moves one or more sentences. A sentence is a collection of words terminated by a punctuation character, such as a period.

textedit - Moves to the start or end of the original range.

### Count

 Data-type
:   Number

**Integer** that specifies the number of units to move. This can be positive or negative. The default is **1**.

## Return Value

Returns an object of type NumberNumber

Integer that returns the number of units moved

**Needs Examples**: This section should include examples.

## Notes

### Remarks

### Syntax

### Standards information

There are no standards that apply here.
