{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=indexFrom
|Data type=any
|Description='''Integer''' that specifies the index in the [[dom/HTMLElement/rows|'''rows''']] collection of the table row that is moved.
|Optional=No
}}{{Method Parameter
|Name=indexTo
|Data type=any
|Description='''Integer''' that specifies where the row is moved within the [[dom/HTMLElement/rows|'''rows''']] collection.
|Optional=No
}}
|Method_applies_to=dom/Window
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Object

Object. Returns a reference to the table row that is moved.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''moveRow''' method to exchange the first and second rows in a table when the user clicks a button.
|Code=&lt;SCRIPT&gt;
function fnMove(){
   oTable.moveRow(0,1);
}
&lt;/SCRIPT&gt;
&lt;INPUT TYPE{{=}}"button" VALUE{{=}}"Change Rows" onclick{{=}}"fnMove()"&gt;
&lt;TABLE ID{{=}}"oTable"&gt;
&lt;TR&gt;&lt;TD&gt;Cell 1, Row 1&lt;/TD&gt;&lt;/TR&gt;
&lt;TR&gt;&lt;TD&gt;Cell 1, Row 2&lt;/TD&gt;&lt;/TR&gt;
&lt;/TABLE&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
Rows between the ''indexFrom'' and ''indexTo'' positions in the [[dom/HTMLElement/rows|'''rows''']] collection are shifted based on the direction the row moves.
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