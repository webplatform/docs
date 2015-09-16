---
title: 'tr'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: tr
  topic: html
notes:
  - 'Add compatibility'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLTableRowElement](/dom/HTMLTableRowElement)'
readiness: 'In Progress'
summary: 'The tr element represents a row of cells in a table.'
tags:
  - Markup
  - Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/properties/rowIndex
    - 'dom/properties/rows (table)'
    - dom/methods/insertRow
    - dom/methods/deleteRow
    - dom/properties/cellIndex
    - dom/properties/cellSpacing
    - dom/methods/insertCell
    - dom/methods/deleteCell
    - dom/properties/innerdom/innerHTML
    - dom/properties/innerText
uri: html/elements/tr

---
## Summary

The tr element represents a row of cells in a table.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLTableRowElement](/dom/HTMLTableRowElement)

## Examples

This example uses the **TR** element with the [**TABLE**](/html/elements/table), **TD**, and **TR** elements to create a table with two rows.

``` html
<table>
<tbody>
<tr>
<td>This is the first row.</td>
</tr>
<tr>
<td>This is the second row.</td>
</tr>
</tbody>
</table>
```

This example uses the table object model to dynamically add two rows and two cells to a table when the user clicks a button.

``` html
<script type="application/javascript">
function createRows(){
   // Insert two rows.
   var oRow1=oTable.insertRow(oTable.rows.length);
   var oRow2=oTable.insertRow(oTable.rows.length);

   // Retrieve the rows collection for the table.
   var aRows=oTable.rows;

   // Retrieve the cells collection for the first row.
   var aCells=oRow1.cells;

   // Insert two cells into the first row.
   var oCell1_1=aRows(oRow1.rowIndex).insertCell(aCells.length);
   var oCell1_2=aRows(oRow1.rowIndex).insertCell(aCells.length);

   // Retrieve the cells collection for the second row.
   aCells=oRow2.cells;

   // Insert two cells into the second row.
   var oCell2_1=aRows(oRow2.rowIndex).insertCell(aCells.length);
   var oCell2_2=aRows(oRow2.rowIndex).insertCell(aCells.length);

   // Add regular HTML values to the 4 new cells.
   oCell1_1.innerHTML="<b>Cell 1.1!</b>";
   oCell1_2.innerHTML="<b>Cell 1.2!</b>";
   oCell2_1.innerHTML="<b>Cell 2.1!</b>";
   oCell2_2.innerHTML="<b>Cell 2.2!</b>";
}
</script>
<button onclick="createRows()">Create Rows</button>
<table id="oTable"></table>
```

## Notes

### Remarks

The **TD** and **TH** elements are valid within a row. To change the HTML in the **TR** element, use the table object model. For example, use the [**rowIndex**](/w/index.php?title=dom/properties/rowIndex&action=edit&redlink=1) property or the [**rows**](/w/index.php?title=dom/properties/rows_(table)&action=edit&redlink=1) collection to retrieve a reference to a specific table row. You can add or delete rows using the [**insertRow**](/w/index.php?title=dom/methods/insertRow&action=edit&redlink=1) and [**deleteRow**](/w/index.php?title=dom/methods/deleteRow&action=edit&redlink=1) methods. To retrieve a reference to a specific cell, use the [**cellIndex**](/w/index.php?title=dom/properties/cellIndex&action=edit&redlink=1) property or the [**cells**](/w/index.php?title=dom/properties/cellSpacing&action=edit&redlink=1) collection. You can add or delete cells using the [**insertCell**](/w/index.php?title=dom/methods/insertCell&action=edit&redlink=1) and [**deleteCell**](/w/index.php?title=dom/methods/deleteCell&action=edit&redlink=1) methods. To change the content of a particular cell, use the [**innerHTML**](/w/index.php?title=dom/properties/innerdom/innerHTML&action=edit&redlink=1) or [**innerText**](/w/index.php?title=dom/properties/innerText&action=edit&redlink=1) property. The [**table**](/html/elements/table) object and its associated elements have a separate table object model, which uses different methods than the general object model. For more information on the table object model, see Building Tables Dynamically. Windows Internet Explorer 8 will only render tables up to 1000 columns. To force Windows Internet Explorer 7 rendering mode, see How Do I Take Advantage of the New Features in Internet Explorer 8.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/tabular-data.html#the-tr-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/tabular-data.html#the-tr-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/tables.html#edef-TR)
:   W3C Recommendation

## See also

### Related pages

-   `Reference`
-   table[table](/html/elements/table)
-   borderCollapse[borderCollapse](/css/properties/border-collapse)
-   `Conceptual`
-   `Building Tables Dynamically`
