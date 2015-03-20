{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add compatibility
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The <code>tr</code> element represents a row of cells in a table.}}
{{Markup_Element
|DOM_interface=dom/HTMLTableRowElement
|Tag_omissions=Closing tag required
|CSS_display=table
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following examples show how to create a table row in HTML and script.
|Code=<nowiki><table>
<tbody>
<tr>
<td>This is the first row.</td>
</tr>
<tr>
<td>This is the second row.</td>
</tr>
</tbody>
</table></nowiki>
|LiveURL=This example uses the '''TR''' element with the [[html/elements/table|'''TABLE''']], '''TD''', and '''TR''' elements to create a table with two rows.
}}{{Single Example
|Language=HTML
|Description=This example uses the table object model to dynamically add two rows and two cells to a table when the user clicks a button.
|Code=<nowiki><script type="application/javascript">
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
<buttononclick="createRows()">Create Rows</button>
<table id="oTable"></table></nowiki>
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''TD''' and '''TH''' elements are valid within a row.
To change the HTML in the '''TR''' element, use the table object model. For example, use the [[dom/properties/rowIndex|'''rowIndex''']] property or the [[dom/properties/rows (table)|'''rows''']] collection to retrieve a reference to a specific table row. You can add or delete rows using the [[dom/methods/insertRow|'''insertRow''']] and [[dom/methods/deleteRow|'''deleteRow''']] methods. To retrieve a reference to a specific cell, use the [[dom/properties/cellIndex|'''cellIndex''']] property or the [[dom/properties/cellSpacing|'''cells''']] collection. You can add or delete cells using the [[dom/methods/insertCell|'''insertCell''']] and [[dom/methods/deleteCell|'''deleteCell''']] methods. To change the content of a particular cell, use the [[dom/properties/innerdom/innerHTML|'''innerHTML''']] or [[dom/properties/innerText|'''innerText''']] property.
The [[html/elements/table|'''table''']] object and its associated elements have a separate table object model, which uses different methods than the general object model.  For more information on the table object model, see Building Tables Dynamically.
Windows Internet Explorer 8 will only render tables up to 1000 columns. To force Windows Internet Explorer 7 rendering mode, see How Do I Take Advantage of the New Features in Internet Explorer 8.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/tabular-data.html#the-tr-element
|Status=W3C Working Draft
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/tabular-data.html#the-tr-element
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/tables.html#edef-TR
|Status=W3C Recommendation
}}
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>Reference</code>
*<code>[[html/elements/table|table]]</code>
*<code>[[css/properties/border-collapse|borderCollapse]]</code>
*<code>Conceptual</code>
*<code>Building Tables Dynamically</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}