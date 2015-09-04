---
title: insertData
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Inserts a new character string into the node at the specified offset.'
uri: dom/CharacterData/insertData

---
# insertData

## Summary

Inserts a new character string into the node at the specified offset.

*Method of [dom/CharacterData](/dom/CharacterData)*

## Syntax

``` {.js}
 textualNode.insertData(offset, text);
```

## Parameters

### offset

 Data-typeÂ
:   String

 The zero-based offset from which to start.

### text

 Data-typeÂ
:   String

 The new character string.

## Return Value

No return value

## Examples

``` {.js}
//create text node
var phrase = document.createTextNode ("A flawed plan today is better than a perfect plan tomorrow.");
//insert "much " (note trailing space)
phrase.insertData(23, "much ");
//report result
alert(phrase.data);
```

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

