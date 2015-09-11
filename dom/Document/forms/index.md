---
title: forms
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs compat table'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Document
    href: /dom/Document
  return:
    predicate: 'Returns an object of type '
    value: 'DOM Node'
    href: /dom/Document
standardization_status: 'W3C Recommendation'
summary: 'This property returns an object array representing an HTMLCollection of all the forms in the document.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Document/forms

---
## <span>Summary</span>

This property returns an object array representing an HTMLCollection of all the forms in the document.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var HTMLCollection = document.forms;
```

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Returns a collection of all the forms of a document

## <span>Examples</span>

``` js
//retrieve forms collection and report how many forms are in the document
function numForms() {
  var allForms = document.forms;
  alert(allForms.length);
}
```

## <span>Related specifications</span>

[DOM Level 2 HTML](http://www.w3.org/TR/DOM-Level-2-HTML/html.html#ID-1689064)
:   Recommendation
