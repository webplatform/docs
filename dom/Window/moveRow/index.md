{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=indexFrom|Data type=Integer|Description='''Integer''' that specifies the index in the [[dom/properties/rows (table)|'''rows''']] collection of the table row that is moved.|Optional=}}
{{Method Parameter|Name=indexTo|Data type=Integer|Description='''Integer''' that specifies where the row is moved within the [[dom/properties/rows (table)|'''rows''']] collection.|Optional=}}
|Method_applies_to=dom/Window
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Object

Object. Returns a reference to the table row that is moved.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''moveRow''' method to exchange the first and second rows in a table when the user clicks a button.
|LiveURL=
|Code=
&lt;SCRIPT&gt;
function fnMove(){
   oTable.moveRow(0,1);
}
&lt;/SCRIPT&gt;
&lt;INPUT TYPE{{=}}"button" VALUE{{=}}"Change Rows" onclick{{=}}"fnMove()"&gt;
&lt;TABLE ID{{=}}"oTable"&gt;
&lt;TR&gt;&lt;TD&gt;Cell 1, Row 1&lt;/TD&gt;&lt;/TR&gt;
&lt;TR&gt;&lt;TD&gt;Cell 1, Row 2&lt;/TD&gt;&lt;/TR&gt;
&lt;/TABLE&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Rows between the ''indexFrom'' and ''indexTo'' positions in the [[dom/properties/rows (table)|'''rows''']] collection are shifted based on the direction the row moves.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[html/elements/table|table]]</code>
*<code>tBody</code>
*<code>tFoot</code>
*<code>tHead</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}