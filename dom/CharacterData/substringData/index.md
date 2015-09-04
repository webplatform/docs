---
title: substringData
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Extracts a range of characters from the node.'
uri: dom/CharacterData/substringData

---
# substringData

## Summary

Extracts a range of characters from the node.

*Method of [dom/CharacterData](/dom/CharacterData)*

## Syntax

``` {.js}
var substring = textualNode.substringData(offset, count);
```

## Parameters

### offset

 Data-typeÂ
:   String

 The zero-based offset from which to start.

### count

 Data-typeÂ
:   String

 The number of characters to extract.

## Return Value

Returns an object of type String.

The requested substring.

## Examples

``` {.js}
//create text node
var phrase = document.createTextNode ("A flawed plan today is way better than a perfect plan tomorrow.");
//retrieve substring "way"
var subst = phrase.substringData(23, 3);
//report result
alert(subst);
```

## Notes

If the sum of the *offset* and *count* parameters exceeds the number of characters in the object, then an error is returned.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 3 Core Specification](http://go.microsoft.com/fwlink/p/?linkid=182717), Section 1.4

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

