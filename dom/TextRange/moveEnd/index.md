---
title: moveEnd
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: Non-Standard
notes:
  - 'needs example'
summary: 'Changes the end position of the range.'
uri: dom/TextRange/moveEnd

---
# moveEnd

## Summary

Changes the end position of the range.

*Method of [dom/TextRange](/dom/TextRange)*

## Syntax

``` {.js}
var result = textRange.moveEnd(/* see parameter list */);
```

## Parameters

### Unit

 Data-typeÂ
:   BSTR

**String**Â that specifies the units to move, using one of the following values:

character - Moves one or more characters.

word - Moves one or more words. A word is a collection of characters terminated by a space or some other white-space character, such as a tab.

sentence - Moves one or more sentences. A sentence is a collection of words terminated by a punctuation character, such as a period.

textedit - Moves to the start or end of the original range.

### Count

 Data-typeÂ
:   Number

**Integer**Â that specifies the number of units to move. This can be positive or negative. The default is **1**.

## Return Value

Returns an object of type Number.

Integer that returns the number of units moved

**Needs Examples**: This section should include examples.

## Notes

### Remarks

### Syntax

### Standards information

There are no standards that apply here.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[moveEnd Method](http://msdn.microsoft.com/en-us/library/ie/ms536620(v=vs.85).aspx) Article]

