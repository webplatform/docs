---
title: 'createTBody'
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
uri: dom/HTMLTableElement/createTBody

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [dom/HTMLTableElement](/dom/HTMLTableElement)[dom/HTMLTableElement](/dom/HTMLTableElement)

## Syntax

``` js
var object = object.createTBody();
```

## Return Value

Returns an object of type DOM NodeDOM Node

Object

**tBody**

null

## Examples

This example uses the **createTBody** method to create a table body.

``` html
myTBody = document.all.myTable.createTBody()
```

## Notes

### Remarks

If a **tBody** already exists, **createTBody** returns the existing element. Otherwise, it returns a pointer to the element created.

### Syntax

### Standards information

There are no standards that apply here.

## See also

### Related pages

-   table[table](/html/elements/table)
