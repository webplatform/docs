---
title: insertData
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/CharacterData
    href: /dom/CharacterData
standardization_status: 'W3C Recommendation'
summary: 'Inserts a new character string into the node at the specified offset.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/CharacterData/insertData

---
## <span>Summary</span>

Inserts a new character string into the node at the specified offset.

Method of [dom/CharacterData](/dom/CharacterData)[dom/CharacterData](/dom/CharacterData)

## <span>Syntax</span>

``` js
 textualNode.insertData(offset, text);
```

## <span>Parameters</span>

### <span>offset</span>

 Data-type
:   String

 The zero-based offset from which to start.

### <span>text</span>

 Data-type
:   String

 The new character string.

## <span>Return Value</span>

No return value

## <span>Examples</span>

``` js
//create text node
var phrase = document.createTextNode ("A flawed plan today is better than a perfect plan tomorrow.");
//insert "much " (note trailing space)
phrase.insertData(23, "much ");
//report result
alert(phrase.data);
```

## <span>Related specifications</span>

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
