---
title: 'appendData'
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
  - API_Object_Methods
  - DOM
uri: dom/CharacterData/appendData

---
## Summary

Appends a string to the end of the character data.

Method of [dom/CharacterData](/dom/CharacterData)[dom/CharacterData](/dom/CharacterData)

## Syntax

``` js
 textualNode.appendData(text);
```

## Parameters

### text

 Data-type
:   String

 The new character string.

## Return Value

No return value

## Examples

``` js
//create text node
var phrase = document.createTextNode("A flawed plan today");
//append string to node (note initial space)
phrase.appendData(" is better than a perfect plan tomorrow.");
```

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
