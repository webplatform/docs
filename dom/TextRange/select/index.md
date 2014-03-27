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
|Parameters=
|Method_applies_to=dom/TextRange
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
This method causes the current object to be highlighted.
When applied to a [[dom/TextRange|'''TextRange''']] object, the select method causes the current object to be highlighted. The following function uses the '''findText''' method to set the current object to the text in the '''TextRange''' object. The function assumes an element that contains the text string "text here".
 <code>function TextRangeSelect() {
 	var r {{=}} document.body.createTextRange();
 	r.findText("text here");
 	r.select();
 }
 </code>
This method produces a shaded rectangle around the elements in the [[dom/HTMLElement/controlRange|'''controlRange''']].
When applied to a '''controlRange''' collection, the select method produces a shaded rectangle around the elements in the '''controlRange'''. The following function uses the add method to set the current object to an element in the '''controlRange''' collection. The function assumes an element with an id of "aaa".
 <code>
 function ControlRangeSelect() {
 	var r {{=}} document.body.createControlRange();
 	r.add(document.all.aaa);
 	r.select();
 }
 </code>
This feature might not be available on non-Microsoft Win32 platforms.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5
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