---
title: readyState
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, clean-up of MSDN import'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLElement/readyState

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var result = element.readyState;
element.readyState = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

An object's state is initially set to **uninitialized**, and then to **loading**. When data loading is complete, the state of the link object passes through the **loaded** and **interactive** states to reach the **complete** state. The states through which an object passes are determined by that object; an object can skip certain states (for example, **interactive**) if the state does not apply to that object. Data source objects and databound elements are normally populated asynchronously, and certain programmatic operations can only be performed reliably on databound objects when they are ready for use. Therefore, the appropriate code should be written to confirm the **readyState** of objects prior to performing certain operations on them. For example, walking the rows of a [**table**](/html/elements/table) should not be attempted until after the **table** has reached the **complete** state. The **readyState** property enables the status of an object to be tested. The correct place to test the **readyState** property is in the event handler for [**onreadystatechange**](/dom/Element/readystatechange). Similarly, a data source object (DSO) fires the [**ondatasetcomplete**](/dom/Event/datasetcomplete) event to notify the document that the dataset is ready for programmatic operation.

### Syntax
