---
title: add
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'compatibility, examples'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/HTMLSelectElement
    href: /dom/HTMLSelectElement
standardization_status: 'W3C Recommendation'
summary: 'Adds an option element to the select element.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/HTMLSelectElement/add

---
## <span>Summary</span>

Adds an option element to the select element.

Method of [dom/HTMLSelectElement](/dom/HTMLSelectElement)[dom/HTMLSelectElement](/dom/HTMLSelectElement)

## <span>Syntax</span>

``` js
 select.add(element, beforeElement);
```

## <span>Parameters</span>

### <span>element</span>

 Data-type
:   DOM Node

 The [option](/dom/HTMLOptionElement) element to add.

### <span>beforeElement</span>

 Data-type
:   DOM Node

 The element before which the new option will be placed. If no value is given, the method places the element at the end of the collection.

## <span>Return Value</span>

No return value

**Needs Examples**: This section should include examples.

## <span>Usage</span>

     This method adds an option element to a select block.

## <span>Notes</span>

Before you can add an element to a collection, you must create it first by using the [**createElement**](/dom/Document/createElement) method.

## <span>Related specifications</span>

[DOM Level 2 HTML](http://www.w3.org/TR/DOM-Level-2-HTML/)
:   Recommendation
