---
title: deleteRow
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
notes:
  - 'summary, clean-up of MSDN import'
uri: dom/HTMLTableElement/deleteRow

---
# deleteRow

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [dom/HTMLTableElement](/dom/HTMLTableElement)*

## Syntax

``` {.js}
var object = object.deleteRow(index);
```

## Parameters

### index

 Data-typeÂ
:   any

**Integer**Â that specifies the zero-based position in the **rows** collection of the row to remove.

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

This example uses the **deleteRow** method to delete the specified row (**tr**) in the [**table**](/html/elements/table).

    document.all.myTable.deleteRow()

## Notes

### Remarks

If you delete a row from a **tFoot**, **tBody**, or **tHead**, you also remove the row from the **rows** collection for the [**table**](/html/elements/table). Deleting a row in the **table** also removes a row from the **rows** collection for the **tBody**. If you delete a row from a **tFoot**, **tBody**, or **tHead**, *index* must contain the [**sectionRowIndex**](/dom/HTMLElement/sectionRowIndex) of the **tr**. When deleting a row from the [**table**](/html/elements/table), *index* must contain the [**rowIndex**](/dom/HTMLElement/rowIndex) of the **tr**.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5

## See also

### Related pages (MSDN)

-   `table`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

