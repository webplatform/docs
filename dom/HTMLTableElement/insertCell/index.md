---
title: 'insertCell'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, clean-up of MSDN import'
readiness: 'In Progress'
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
uri: dom/HTMLTableElement/insertCell

---
Method of [dom/HTMLTableElement](/dom/HTMLTableElement)[dom/HTMLTableElement](/dom/HTMLTableElement)

## Syntax

``` js
var object = object.insertCell(index);
```

## Parameters

### index

 Data-type
:   any

**Integer** that specifies where to insert the cell in the **tr**. The default value is **-1**, which appends the new cell to the end of the **cells** collection.

## Return Value

Returns an object of type DOM NodeDOM Node

Object

Returns the **td** element object if successful, or null otherwise.

## Examples

This example uses the **insertCell** method to add a cell to the end of the **tr**.

``` html
myNewCell = document.all.myTable.rows[0].insertCell()
```

## Notes

### Remarks

The preferred technique for inserting a cell is to add the cell at the end of the **cells** collection. It is faster to add a cell at the end of a row than somewhere in the middle. To add a cell at the end of the collection, specify the `-1` value, or the length of the **cells** collection minus `1`.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5
