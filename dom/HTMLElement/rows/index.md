---
title: rows
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rows-cells.htm'
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
uri: dom/HTMLElement/rows

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## <span>Syntax</span>

``` js
var result = element.rows;
element.rows = value;
```

## <span>Examples</span>

This example shows how to use the **rows** and **cells** collections to insert a number into each cell of the table.

``` html
&lt;HTML&gt;
&lt;SCRIPT type="text/javascript"&gt;
function numberCells()
{
    var count=1;
    var oTable = document.getElementById('oTable');
    var RowsLength = oTable.rows.length;
    for (var i=0; i &lt; RowsLength; i++)
    {
        var oCells = oTable.rows.item(i).cells;
        var CellsLength = oCells.length;
        for (var j=0; j &lt; CellsLength; j++)
        {
            oCells.item(j).innerHTML = count++;
        }
    }
}
&lt;/SCRIPT&gt;
&lt;BODY onload="numberCells()"&gt;
&lt;TABLE id=oTable border=1&gt;
&lt;TR&gt;&lt;TH&gt;&amp;nbsp;&lt;/TH&gt;&lt;TH&gt;&amp;nbsp;&lt;/TH&gt;&lt;TH&gt;&amp;nbsp;&lt;/TH&gt;&lt;TH&gt;&amp;nbsp;&lt;/TH&gt;&lt;/TR&gt;
&lt;TR&gt;&lt;TD&gt;&amp;nbsp;&lt;/TD&gt;&lt;TD&gt;&amp;nbsp;&lt;/TD&gt;&lt;TD&gt;&amp;nbsp;&lt;/TD&gt;&lt;TD&gt;&amp;nbsp;&lt;/TD&gt;&lt;/TR&gt;
&lt;TR&gt;&lt;TD&gt;&amp;nbsp;&lt;/TD&gt;&lt;TD&gt;&amp;nbsp;&lt;/TD&gt;&lt;TD&gt;&amp;nbsp;&lt;/TD&gt;&lt;TD&gt;&amp;nbsp;&lt;/TD&gt;&lt;/TR&gt;
&lt;/TABLE&gt;
&lt;/BODY&gt;&lt;/HTML&gt;
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rows-cells.htm)

## <span>Notes</span>

### <span>Remarks</span>

The scope of the **rows** collection is for the **tHead**, **tBody**, or **tFoot** object of the table. In addition, there is also a **rows** collection for the [**table**](/html/elements/table) object, which contains all the rows for the entire table. A row that appears in one of the table sections also appears in the **rows** collection for the **table**. The **tr** object has two index properties, [**rowIndex**](/dom/HTMLElement/rowIndex) and [**sectionRowIndex**](/dom/HTMLElement/sectionRowIndex), that indicate where a given row appears. The **rowIndex** property indicates where the **tr** appears with respect to the **rows** collection for the whole table. By contrast, **sectionRowIndex** returns where the **tr** appears with respect to the **rows** collection for the specific table section in which it is located. If duplicate identifiers are found, a collection of those items is returned. Collections of duplicates must be referenced subsequently by ordinal position.

### <span>Syntax</span>

### <span>Standards information</span>

There are no standards that apply here.