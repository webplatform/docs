---
title: 'deleteData'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/CharacterData
    href: /dom/CharacterData
standardization_status: 'W3C Recommendation'
summary: 'Removes a specified range of characters from the node.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/CharacterData/deleteData

---
## Summary

Removes a specified range of characters from the node.

Method of [dom/CharacterData](/dom/CharacterData)[dom/CharacterData](/dom/CharacterData)

## Syntax

``` js
 textualNode.deleteData(offset, count);
```

## Parameters

### offset

 Data-type
:   String

 The zero-based character offset from which to start.

### count

 Data-type
:   String

 The number of characters to remove.

## Return Value

No return value

## Examples

``` js
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

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
