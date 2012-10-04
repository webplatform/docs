{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=index|Data type=Integer|Description='''Integer''' that specifies the zero-based position in the [[dom/properties/rows (table)|'''rows''']] collection of the row to remove.|Optional=}}
|Method_applies_to=dom/HTMLTableElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''deleteRow''' method to delete the specified row ('''tr''') in the [[html/elements/table|'''table''']].
|LiveURL=
|Code=
document.all.myTable.deleteRow()
}}}}
{{Notes_Section
|Notes=
===Remarks===
If you delete a row from a '''tFoot''', '''tBody''', or '''tHead''', you also remove the row from the [[dom/properties/rows (table)|'''rows''']] collection for the [[html/elements/table|'''table''']]. Deleting a row in the '''table''' also removes a row from the '''rows''' collection for the '''tBody'''.
If you delete a row from a '''tFoot''', '''tBody''', or '''tHead''', ''index'' must contain the [[dom/properties/sectionRowIndex|'''sectionRowIndex''']] of the '''tr'''. When deleting a row from the [[html/elements/table|'''table''']], ''index'' must contain the [[dom/properties/rowIndex|'''rowIndex''']] of the '''tr'''.
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
*<code>[[dom/methods/insertRow|insertRow]]</code>
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