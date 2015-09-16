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
## Summary

Extracts a range of characters from the node.

Method of [dom/CharacterData](/dom/CharacterData)[dom/CharacterData](/dom/CharacterData)

## Syntax

``` js
var substring = textualNode.substringData(offset, count);
```

## Parameters

### offset

 Data-type
:   String

 The zero-based offset from which to start.

### count

 Data-type
:   String

 The number of characters to extract.

## Return Value

Returns an object of type StringString

The requested substring.

## Examples

``` js
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

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
