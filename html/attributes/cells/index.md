---
title: cells
tags:
  - Markup
  - Attributes
  - HTML
readiness: 'Not Ready'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
summary: 'Retrieves a collection of all cells in the table row or in the entire table.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/cellSpacing.htm'
uri: html/attributes/cells

---
# cells

## Summary

Retrieves a collection of all cells in the table row or in the entire table.

Applies to
:    ?

## Examples

This example uses the **cellspacing** attribute and the **cellSpacing** property to change the spacing between two cells.

    <table id="oTable" border="0" cellspacing="10">
        <tr>
            <td>Cell 1</td>
            <td>Cell 2</td>
        </tr>
    </table>
    :
    <button onclick="oTable.cellSpacing=20">Larger spacing</button>
    <button onclick="oTable.cellSpacing=5">Smaller spacing</button>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/cellSpacing.htm)

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5
-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 11.3.3

## See also

### Related pages (MSDN)

-   `table`
-   `cellPadding`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

