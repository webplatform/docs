---
title: replaceData
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
  - API
  - Object
  - Methods
  - DOM
uri: dom/CharacterData/replaceData

---
## <span>Summary</span>

Replaces a specified range of characters in the node with a new character string.

Method of [dom/CharacterData](/dom/CharacterData)[dom/CharacterData](/dom/CharacterData)

## <span>Syntax</span>

``` js
 textualNode.replaceData(offset, count, text);
```

## <span>Parameters</span>

### <span>offset</span>

 Data-type
:   String

 The zero-based offset from which to start.

### <span>count</span>

 Data-type
:   String

 The number of characters to replace.

### <span>text</span>

 Data-type
:   String

 The new character string.

## <span>Return Value</span>

No return value

## <span>Examples</span>

``` html
//create text node
var phrase = document.createTextNode ("A flawed plan today is much better than a perfect plan tomorrow.");
//replace "much" with "way"
phrase.replaceData(23, 4, "way");
//report result
alert(phrase.data);
```

## <span>Notes</span>

If the sum of the *offset* and *count* parameters exceeds the number of characters in the object, then all the characters from the offset to the end of the data are replaced.

## <span>Related specifications</span>

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
