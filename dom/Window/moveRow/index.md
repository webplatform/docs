{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Moves a table row to a new position.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=indexFrom
|Data type=Number
|Description='''Integer''' that specifies the index in the [[dom/HTMLElement/rows|'''rows''']] collection of the table row that is moved. -1 Default.
|Optional=No
}}{{Method Parameter
|Name=indexTo
|Data type=Number
|Description='''Integer''' that specifies where the row is moved within the [[dom/HTMLElement/rows|'''rows''']] collection. -1 Default.
|Optional=No
}}
|Method_applies_to=dom/Window
|Example_object_name=oTable
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example uses the '''moveRow''' method to exchange the first and second rows in a table when the user clicks a button.
|Code=&lt;script type{{=}}"text/javascript&gt;
function fnMove(){
   oTable.moveRow(0,1);
}
&lt;/script&gt;
&lt;input type{{=}}"button" value{{=}}"Change Rows" onclick{{=}}"fnMove()"&gt;
&lt;table id{{=}}"oTable"&gt;
&lt;tr&gt;&lt;td&gt;Cell 1, Row 1&lt;/td&gt;&lt;/tr&gt;
&lt;tr&gt;&lt;td&gt;Cell 1, Row 2&lt;/td&gt;&lt;/tr&gt;
&lt;/table&gt;
}}
}}
{{Notes_Section
|Usage=Use to re-order rows of tabula data.
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536622(v=vs.85).aspx moveRow Method]
|HTML5Rocks_link=
}}