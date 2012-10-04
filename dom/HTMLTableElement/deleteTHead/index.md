{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters=
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
|Description=This example uses the '''deleteTHead''' method to delete the '''tHead''' element from the table.
|LiveURL=
|Code=
document.all.myTable.deleteTHead()
}}}}
{{Notes_Section
|Notes=
===Remarks===
If only one '''tHead''' element 
exists in the source, the '''deleteTHead''' 
method deletes the table header. If multiple '''tHead''' 
elements have been defined, the next '''tHead''' element 
in the source order is promoted as the table header.
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
*<code>Reference</code>
*<code>[[dom/methods/createCaption|createCaption]]</code>
*<code>[[dom/methods/createTFoot|createTFoot]]</code>
*<code>[[dom/methods/createTHead|createTHead]]</code>
*<code>[[dom/methods/deleteCaption|deleteCaption]]</code>
*<code>[[dom/methods/deleteTFoot|deleteTFoot]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}