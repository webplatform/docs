---
title: insertRow
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
notes:
  - 'summary, clean-up of MSDN import'
uri: dom/HTMLTableElement/insertRow

---
# insertRow

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [dom/HTMLTableElement](/dom/HTMLTableElement)*

## Syntax

``` {.js}
var object = object.insertRow(index);
```

## Parameters

### index

 Data-typeÂ
:   any

**Integer**Â that specifies where to insert the row in the **rows** collection. The default value is **-1**, which appends the new row to the end of the **rows** collection.

## Return Value

Returns an object of type DOM Node.

Object

**tr**

null

## Examples

This example uses the **insertRow** method to add a row to the [**table**](/html/elements/table).

    myNewRow = document.all.myTable.insertRow()

## Notes

### Remarks

The preferred technique for inserting a row is to add the row at the end of the **rows** collection. It is faster to add a row at the end of a table than somewhere in the middle. To add a row at the end of the collection, specify the `-1` value, or the length of the **rows** collection minus `1`.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5

## See also

### Related pages (MSDN)

-   `table`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

