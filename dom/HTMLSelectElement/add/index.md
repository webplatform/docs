---
title: add
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'compatibility, examples'
summary: 'Adds an option element to the select element.'
uri: dom/HTMLSelectElement/add

---
# add

## Summary

Adds an option element to the select element.

*Method of [dom/HTMLSelectElement](/dom/HTMLSelectElement)*

## Syntax

``` {.js}
 select.add(element, beforeElement);
```

## Parameters

### element

 Data-typeÂ
:   DOM Node

 The [option](/dom/HTMLOptionElement) element to add.

### beforeElement

 Data-typeÂ
:   DOM Node

 The element before which the new option will be placed. If no value is given, the method places the element at the end of the collection.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Usage

     This method adds an option element to a select block.

## Notes

Before you can add an element to a collection, you must create it first by using the [**createElement**](/dom/Document/createElement) method.

## Related specifications

Specification
:   Status
[DOM Level 2 HTML](http://www.w3.org/TR/DOM-Level-2-HTML/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

