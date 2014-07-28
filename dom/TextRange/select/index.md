{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Not sure if this http://www.w3.org/TR/DOM-Level-2-HTML/html is a standard or not.... the MSDN doco has not w3 ref.... see Elliot/MSFT.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Makes the selection equal to the current object. }}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/TextRange
|Example_object_name=range
|Return_value_name=result
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=When applied to a TextRange object, the select method causes the current object to be highlighted. The following function uses the findText method to set the current object to the text in the TextRange object. The function assumes an element that contains the text string "text here".
|Code=function TextRangeSelect() {
	var r {{=}} document.body.createTextRange();
	r.findText("text here");
	r.select();
}
}}{{Single Example
|Language=JavaScript
|Description=When applied to a controlRange collection, the select method produces a shaded rectangle around the elements in the controlRange. The following function uses the add method to set the current object to an element in the controlRange collection. The function assumes an element with an id of "aaa".
|Code=function ControlRangeSelect() {
	var r {{=}} document.body.createControlRange();
	r.add(document.all.aaa);
	r.select();
}
}}
}}
{{Notes_Section
|Usage=Used to programmatically select/highlight text and/or controls in a web document.
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536735(v=vs.85).aspx select Method]
|HTML5Rocks_link=
}}