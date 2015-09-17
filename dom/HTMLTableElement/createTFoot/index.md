---
title: 'createTFoot'
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
  - API_Object_Methods
  - DOM
  - Needs_Summary
uri: dom/HTMLTableElement/createTFoot

---
Method of [dom/HTMLTableElement](/dom/HTMLTableElement)[dom/HTMLTableElement](/dom/HTMLTableElement)

## Syntax

``` js
var object = object.createTFoot();
```

## Return Value

Returns an object of type DOM NodeDOM Node

Object

**tFoot**

null

## Examples

This example uses the **createTFoot** method to create a table footer.

``` html
myTFoot = document.all.myTable.createTFoot()
```

## Notes

### Remarks

If a **tFoot** already exists for the [**table**](/html/elements/table), the **createTFoot** method returns the existing element. Otherwise, it returns a pointer to the element created.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5

## See also

### Related pages

-   table[table](/html/elements/table)
