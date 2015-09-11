---
title: substringData
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/CharacterData
    href: /dom/CharacterData
  return_type:
    predicate: 'Returns an object of type  '
    value: String
    href: /dom/CharacterData
standardization_status: 'W3C Recommendation'
summary: 'Extracts a range of characters from the node.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/CharacterData/substringData

---
## <span>Summary</span>

Extracts a range of characters from the node.

Method of [dom/CharacterData](/dom/CharacterData)[dom/CharacterData](/dom/CharacterData)

## <span>Syntax</span>

``` js
var substring = textualNode.substringData(offset, count);
```

## <span>Parameters</span>

### <span>offset</span>

 Data-type
:   String

 The zero-based offset from which to start.

### <span>count</span>

 Data-type
:   String

 The number of characters to extract.

## <span>Return Value</span>

Returns an object of type StringString

The requested substring.

## <span>Examples</span>

``` js
//create text node
var phrase = document.createTextNode ("A flawed plan today is way better than a perfect plan tomorrow.");
//retrieve substring "way"
var subst = phrase.substringData(23, 3);
//report result
alert(subst);
```

## <span>Notes</span>

If the sum of the *offset* and *count* parameters exceeds the number of characters in the object, then an error is returned.

### <span>Syntax</span>

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 3 Core Specification](http://go.microsoft.com/fwlink/p/?linkid=182717), Section 1.4

## <span>Related specifications</span>

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
