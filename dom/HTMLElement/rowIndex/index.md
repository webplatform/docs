---
title: rowIndex
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'summary, clean-up of MSDN import'
uri: dom/HTMLElement/rowIndex

---
# rowIndex

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLElement](/dom/HTMLElement)</span></span>

## Syntax

``` {.js}
var result = element.rowIndex;
element.rowIndex = value;
```

## Examples

This example function shows how to use the **rowIndex** attribute to format a [**table**](/html/elements/table). The function sets the background color of the rows in the **table** to black or white, alternating row by row.

    function formatTable(oTable)
    {
      var rows=oTable.rows;
      for(var i=0;i<rows.length;i++)
      {
        if(i%2==0) {
          rows[i].style.backgroundColor = "black";
          rows[i].style.color = "white";
        } else {
          rows[i].style.backgroundColor = "white";
          rows[i].style.color = "black";
        }
      }
    }

## Notes

### Remarks

This property is different from [**sectionRowIndex**](/dom/HTMLElement/sectionRowIndex), which indicates the object's position in the **tBody**, **tHead**, or **tFoot** [**rows**](/dom/HTMLElement/rows) collection. These sections are mutually exclusive, so the **tr** is always contained in one of these sections and in the [**table**](/html/elements/table). You can determine the **rowIndex** property of an object by the order in which the object appears in the HTML source.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

