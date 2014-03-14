{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/HTMLTableElement
|Read_only=No
|Example_object_name=table
|Return_value_name=cellSpacing
|Javascript_data_type=Number
|Example_value_name=newCellSpacing
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example shows how to use the '''rows''' collection on the [[html/elements/table|'''table''']] object and the '''cells''' collection to insert a number into each cell of the table.
|Code=&lt;!doctype html&gt;
&lt;html&gt;
 &lt;head&gt;
  &lt;script&gt;
function numberCells() {
  var count {{=}} 1;
  var oTable {{=}} document.getElementById('oTable');
  var rowsLength {{=}} oTable.rows.length;
  for (var i{{=}}0; i &lt; rowsLength; i++) {
    var oCells {{=}} oTable.rows.item(i).cells;
    var cellsLength {{=}} oCells.length;
    for (var j{{=}}0; j &lt; cellsLength; j++) {
      oCells.item(j).innerHTML {{=}} count++;
    }
  }
}
  &lt;/script&gt;
 &lt;/head&gt;
 &lt;body onload{{=}}"numberCells()"&gt;
  &lt;table id{{=}}"oTable" border{{=}}"1"&gt;
&lt;tr&gt;&lt;th&gt;&amp;nbsp;&lt;/th&gt;&lt;th&gt;&amp;nbsp;&lt;/th&gt;&lt;th&gt;&amp;nbsp;&lt;/th&gt;&lt;th&gt;&amp;nbsp;&lt;/th&gt;&lt;/tr&gt;
&lt;tr&gt;&lt;td&gt;&amp;nbsp;&lt;/td&gt;&lt;td&gt;&amp;nbsp;&lt;/td&gt;&lt;td&gt;&amp;nbsp;&lt;/td&gt;&lt;td&gt;&amp;nbsp;&lt;/td&gt;&lt;/tr&gt;
&lt;tr&gt;&lt;td&gt;&amp;nbsp;&lt;/td&gt;&lt;td&gt;&amp;nbsp;&lt;/td&gt;&lt;td&gt;&amp;nbsp;&lt;/td&gt;&lt;td&gt;&amp;nbsp;&lt;/td&gt;&lt;/tr&gt;
  &lt;/table&gt;
 &lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rows-cells.htm
}}
}}
{{Notes_Section
|Notes=A '''cells''' collection is comprised of '''th''' and '''td''' objects.
When a cell spans multiple rows, that cell appears only in the '''cells''' collection for the first of the rows that the cell spans.
If duplicate identifiers are found, a collection of those items is returned. Collections of duplicates must be referenced subsequently by ordinal position.
Individual '''cells''' or an array of '''cells''' can be specified using a spreadsheet format. By specifying a colon-delimited string of the starting and ending cells, a '''cells''' collection can be retrieved from anywhere in the table. Specifying a particular cell with this format returns that object. The format of this string uses letters to indicate columns, starting with A, and numbers to indicate rows, starting with 1. A '''cells''' collection on a table row includes only the elements within that row if the ''vIndex'' string specifies a range of multiple rows using the spreadsheet format.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 HTML
|URL=http://www.w3.org/TR/DOM-Level-2-HTML/
|Status=Recommendation
|Relevant_changes=Section 1.6.5
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}