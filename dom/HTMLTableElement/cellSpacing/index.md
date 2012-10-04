{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example shows how to use the [[dom/properties/rows (table)|'''rows''']] collection on the [[html/elements/table|'''table''']] object and the '''cells''' collection to insert a number into each cell of the table.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rows-cells.htm
|Code=
&lt;HTML&gt;
&lt;SCRIPT type{{=}}"text/javascript"&gt;
function numberCells()
{
	var count{{=}}1;
	var oTable {{=}} document.getElementById('oTable');
	var RowsLength {{=}} oTable.rows.length;
	for (var i{{=}}0; i &lt; RowsLength; i++)
	{
	    var oCells {{=}} oTable.rows.item(i).cells;
	    var CellsLength {{=}} oCells.length;
	    for (var j{{=}}0; j &lt; CellsLength; j++) 
	    {
		    oCells.item(j).innerHTML {{=}} count++;
	    }
	}
}
&lt;/SCRIPT&gt;
&lt;BODY onload{{=}}"numberCells()"&gt;
&lt;TABLE id{{=}}oTable border{{=}}1&gt;
&lt;TR&gt;&lt;TH&gt;&amp;nbsp;&lt;/TH&gt;&lt;TH&gt;&amp;nbsp;&lt;/TH&gt;&lt;TH&gt;&amp;nbsp;&lt;/TH&gt;&lt;TH&gt;&amp;nbsp;&lt;/TH&gt;&lt;/TR&gt;
&lt;TR&gt;&lt;TD&gt;&amp;nbsp;&lt;/TD&gt;&lt;TD&gt;&amp;nbsp;&lt;/TD&gt;&lt;TD&gt;&amp;nbsp;&lt;/TD&gt;&lt;TD&gt;&amp;nbsp;&lt;/TD&gt;&lt;/TR&gt;
&lt;TR&gt;&lt;TD&gt;&amp;nbsp;&lt;/TD&gt;&lt;TD&gt;&amp;nbsp;&lt;/TD&gt;&lt;TD&gt;&amp;nbsp;&lt;/TD&gt;&lt;TD&gt;&amp;nbsp;&lt;/TD&gt;&lt;/TR&gt;
&lt;/TABLE&gt;
&lt;/BODY&gt;&lt;/HTML&gt; 
}}}}
{{Notes_Section
|Notes=
===Remarks===
A '''cells''' collection is comprised of '''th''' and '''td''' objects.
When a cell spans multiple rows, that cell appears only in the '''cells''' collection for the first of the rows that the cell spans.
If duplicate identifiers are found, a collection of those items is returned. Collections of duplicates must be referenced subsequently by ordinal position.
Individual '''cells''' or an array of '''cells''' can be specified using a spreadsheet format. By specifying a colon-delimited string of the starting and ending cells, a '''cells''' collection can be retrieved from anywhere in the table. Specifying a particular cell with this format returns that object. The format of this string uses letters to indicate columns, starting with A, and numbers to indicate rows, starting with 1. A '''cells''' collection on a table row includes only the elements within that row if the ''vIndex'' string specifies a range of multiple rows using the spreadsheet format.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5


}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}