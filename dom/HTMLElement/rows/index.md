---
title: rows
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'summary, clean-up of MSDN import'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rows-cells.htm'
uri: dom/HTMLElement/rows

---
# rows

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLElement](/dom/HTMLElement)</span></span>

## Syntax

``` {.js}
var result = element.rows;
element.rows = value;
```

## Examples

This example shows how to use the **rows** and **cells** collections to insert a number into each cell of the table.

    <HTML>
    <SCRIPT type="text/javascript">
    function numberCells()
    {
        var count=1;
        var oTable = document.getElementById('oTable');
        var RowsLength = oTable.rows.length;
        for (var i=0; i < RowsLength; i++)
        {
            var oCells = oTable.rows.item(i).cells;
            var CellsLength = oCells.length;
            for (var j=0; j < CellsLength; j++)
            {
                oCells.item(j).innerHTML = count++;
            }
        }
    }
    </SCRIPT>
    <BODY onload="numberCells()">
    <TABLE id=oTable border=1>
    <TR><TH>&nbsp;</TH><TH>&nbsp;</TH><TH>&nbsp;</TH><TH>&nbsp;</TH></TR>
    <TR><TD>&nbsp;</TD><TD>&nbsp;</TD><TD>&nbsp;</TD><TD>&nbsp;</TD></TR>
    <TR><TD>&nbsp;</TD><TD>&nbsp;</TD><TD>&nbsp;</TD><TD>&nbsp;</TD></TR>
    </TABLE>
    </BODY></HTML>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rows-cells.htm)

## Notes

### Remarks

The scope of the **rows** collection is for the **tHead**, **tBody**, or **tFoot** object of the table. In addition, there is also a **rows** collection for the [**table**](/html/elements/table) object, which contains all the rows for the entire table. A row that appears in one of the table sections also appears in the **rows** collection for the **table**. The **tr** object has two index properties, [**rowIndex**](/dom/HTMLElement/rowIndex) and [**sectionRowIndex**](/dom/HTMLElement/sectionRowIndex), that indicate where a given row appears. The **rowIndex** property indicates where the **tr** appears with respect to the **rows** collection for the whole table. By contrast, **sectionRowIndex** returns where the **tr** appears with respect to the **rows** collection for the specific table section in which it is located. If duplicate identifiers are found, a collection of those items is returned. Collections of duplicates must be referenced subsequently by ordinal position.

### Syntax

### Standards information

There are no standards that apply here.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

