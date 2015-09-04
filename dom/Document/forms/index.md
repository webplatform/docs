---
title: forms
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs compat table'
summary: 'This property returns an object array representing an HTMLCollection of all the forms in the document.'
uri: dom/Document/forms

---
# forms

## Summary

This property returns an object array representing an HTMLCollection of all the forms in the document.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Document](/dom/Document)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var HTMLCollection = document.forms;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">DOM Node</span></span>

Returns a collection of all the forms of a document

## Examples

``` {.js}
//retrieve forms collection and report how many forms are in the document
function numForms() {
  var allForms = document.forms;
  alert(allForms.length);
}
```

## Related specifications

Specification
:   Status
[DOM Level 2 HTML](http://www.w3.org/TR/DOM-Level-2-HTML/html.html#ID-1689064)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

