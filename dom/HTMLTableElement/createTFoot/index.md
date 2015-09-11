---
title: createTFoot
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, clean-up of MSDN import'
readiness: 'Not Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/HTMLTableElement
    href: /dom/HTMLTableElement
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/HTMLTableElement
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/HTMLTableElement/createTFoot

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [dom/HTMLTableElement](/dom/HTMLTableElement)[dom/HTMLTableElement](/dom/HTMLTableElement)

## <span>Syntax</span>

``` js
var object = object.createTFoot();
```

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Object

**tFoot**

null

## <span>Examples</span>

This example uses the **createTFoot** method to create a table footer.

``` html
myTFoot = document.all.myTable.createTFoot()
```

## <span>Notes</span>

### <span>Remarks</span>

If a **tFoot** already exists for the [**table**](/html/elements/table), the **createTFoot** method returns the existing element. Otherwise, it returns a pointer to the element created.

### <span>Syntax</span>

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `table`
