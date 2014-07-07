{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=summary, clean-up of MSDN import
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example shows how to use the '''rows''' and '''cells''' collections to insert a number into each cell of the table.
|Code=&lt;HTML&gt;
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
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rows-cells.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The scope of the '''rows''' collection is for the '''tHead''', '''tBody''', or '''tFoot''' object of the table. In addition, there is also a '''rows''' collection for the [[html/elements/table|'''table''']] object, which contains all the rows for the entire table. A row that appears in one of the table sections also appears in the '''rows''' collection for the '''table'''.
The '''tr''' object has two index properties, [[dom/HTMLElement/rowIndex|'''rowIndex''']] and [[dom/HTMLElement/sectionRowIndex|'''sectionRowIndex''']], that indicate where a given row appears. The '''rowIndex''' property indicates where the '''tr''' appears with respect to the '''rows''' collection for the whole table. By contrast, '''sectionRowIndex''' returns where the '''tr''' appears with respect to the '''rows''' collection for the specific table section in which it is located.
If duplicate identifiers are found, a collection of those items is returned. Collections of duplicates must be referenced subsequently by ordinal position.
|Import_Notes====Syntax===
===Standards information===
There are no standards that apply here.
}}
{{Related_Specifications_Section
|Specifications=
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