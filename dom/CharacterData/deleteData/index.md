---
title: deleteData
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Removes a specified range of characters from the node.'
uri: dom/CharacterData/deleteData

---
# deleteData

## Summary

Removes a specified range of characters from the node.

*Method of [dom/CharacterData](/dom/CharacterData)*

## Syntax

``` {.js}
 textualNode.deleteData(offset, count);
```

## Parameters

### offset

 Data-typeÂ
:   String

 The zero-based character offset from which to start.

### count

 Data-typeÂ
:   String

 The number of characters to remove.

## Return Value

No return value

## Examples

``` {.js}
//create text node
var phrase = document.createTextNode ("A flawed plan today is not better than a perfect plan tomorrow.");
//delete "not " (note trailing space)
phrase.deleteData(23, 4);
//report result
alert(phrase.data);
```

## Usage

     Upon success of this method, the data and length properties reflect the change.

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

