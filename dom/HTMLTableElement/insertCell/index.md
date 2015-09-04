---
title: insertCell
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
notes:
  - 'summary, clean-up of MSDN import'
uri: dom/HTMLTableElement/insertCell

---
# insertCell

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [dom/HTMLTableElement](/dom/HTMLTableElement)*

## Syntax

``` {.js}
var object = object.insertCell(index);
```

## Parameters

### index

 Data-typeÂ
:   any

**Integer**Â that specifies where to insert the cell in the **tr**. The default value is **-1**, which appends the new cell to the end of the **cells** collection.

## Return Value

Returns an object of type DOM Node.

Object

Returns the **td** element object if successful, or null otherwise.

## Examples

This example uses the **insertCell** method to add a cell to the end of the **tr**.

    myNewCell = document.all.myTable.rows[0].insertCell()

## Notes

### Remarks

The preferred technique for inserting a cell is to add the cell at the end of the **cells** collection. It is faster to add a cell at the end of a row than somewhere in the middle. To add a cell at the end of the collection, specify the `-1` value, or the length of the **cells** collection minus `1`.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

