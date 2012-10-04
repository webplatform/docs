{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=index|Data type=Integer|Description='''Integer''' that specifies where to insert the row in the [[dom/properties/rows (table)|'''rows''']] collection. The default value is '''-1''', which appends the new row to the end of the '''rows''' collection.|Optional=}}
|Method_applies_to=dom/HTMLTableElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Object

'''tr'''

null


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''insertRow''' method to add a row to the [[html/elements/table|'''table''']].
|LiveURL=
|Code=
myNewRow {{=}} document.all.myTable.insertRow()
}}}}
{{Notes_Section
|Notes=
===Remarks===
The preferred technique for inserting a row is to add the row at the end of the [[dom/properties/rows (table)|'''rows''']] collection. It is faster to add a row at the end of a table than somewhere in the middle. To add a row at the end of the collection, specify the <code>-1</code> value, or the length of the '''rows''' collection minus <code>1</code>.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[html/elements/table|table]]</code>
*<code>tBody</code>
*<code>tFoot</code>
*<code>tHead</code>
*<code>Reference</code>
*<code>[[dom/properties/rowIndex|rowIndex]]</code>
*<code>[[dom/properties/rows (table)|rows]]</code>
*<code>[[dom/properties/sectionRowIndex|sectionRowIndex]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}