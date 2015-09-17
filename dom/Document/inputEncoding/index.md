---
title: 'inputEncoding'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example and compat tables'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Document
    href: /dom/Document
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Document
standardization_status: Deprecated
summary: 'Gets the character encoding that is used for the text that is loaded into the document object.'
tags:
  - API_Object_Properties
  - DOM
  - Needs_Examples
uri: dom/Document/inputEncoding

---
## Summary

Gets the character encoding that is used for the text that is loaded into the document object.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

**Note**: This property is read-only.

``` js
var inputEncoding = document.inputEncoding;
```

## Return Value

Returns an object of type StringString

The character encoding that is used for the text that is loaded into the **document** object, or null when it is unknown.

## Related specifications

[DOM Level 4](http://www.w3.org/TR/2014/CR-dom-20140508/#dom-core)
:   Candidate Recommendation

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/core.html#Document3-inputEncoding)
:   Recommendation
