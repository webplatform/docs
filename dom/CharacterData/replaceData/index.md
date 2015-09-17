---
title: 'replaceData'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/CharacterData
    href: /dom/CharacterData
standardization_status: 'W3C Recommendation'
summary: 'Replaces a specified range of characters in the node with a new character string.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/CharacterData/replaceData

---
## Summary

Replaces a specified range of characters in the node with a new character string.

Method of [dom/CharacterData](/dom/CharacterData)[dom/CharacterData](/dom/CharacterData)

## Syntax

``` js
 textualNode.replaceData(offset, count, text);
```

## Parameters

### offset

 Data-type
:   String

 The zero-based offset from which to start.

### count

 Data-type
:   String

 The number of characters to replace.

### text

 Data-type
:   String

 The new character string.

## Return Value

No return value

## Examples

``` html
//create text node
var phrase = document.createTextNode ("A flawed plan today is much better than a perfect plan tomorrow.");
//replace "much" with "way"
phrase.replaceData(23, 4, "way");
//report result
alert(phrase.data);
```

## Notes

If the sum of the *offset* and *count* parameters exceeds the number of characters in the object, then all the characters from the offset to the end of the data are replaced.

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
