---
title: appendData
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/CharacterData
    href: /dom/CharacterData
standardization_status: 'W3C Recommendation'
summary: 'Appends a string to the end of the character data.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/CharacterData/appendData

---
## <span>Summary</span>

Appends a string to the end of the character data.

Method of [dom/CharacterData](/dom/CharacterData)[dom/CharacterData](/dom/CharacterData)

## <span>Syntax</span>

``` js
 textualNode.appendData(text);
```

## <span>Parameters</span>

### <span>text</span>

 Data-type
:   String

 The new character string.

## <span>Return Value</span>

No return value

## <span>Examples</span>

``` js
//create text node
var phrase = document.createTextNode("A flawed plan today");
//append string to node (note initial space)
phrase.appendData(" is better than a perfect plan tomorrow.");
```

## <span>Related specifications</span>

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
