{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/TextRange
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
This method causes the current object to be highlighted.
When applied to a [[dom/traversal/TextRange|'''TextRange''']] object, the select method causes the current object to be highlighted. The following function uses the [[dom/traversal/methods/findText|'''findText''']] method to set the current object to the text in the '''TextRange''' object. The function assumes an element that contains the text string "text here".
 <code>function TextRangeSelect() {
 	var r {{=}} document.body.createTextRange();
 	r.findText("text here");
 	r.select();
 }
 </code>
This method produces a shaded rectangle around the elements in the [[dom/properties/controlRange|'''controlRange''']].
When applied to a [[dom/properties/controlRange|'''controlRange''']] collection, the select method produces a shaded rectangle around the elements in the '''controlRange'''. The following function uses the add method to set the current object to an element in the '''controlRange''' collection. The function assumes an element with an id of "aaa".
 <code>
 function ControlRangeSelect() {
 	var r {{=}} document.body.createControlRange();
 	r.add(document.all.aaa);
 	r.select();
 }
 </code>
This feature might not be available on non-Microsoft Win32 platforms.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/traversal/TextRange|TextRange]]</code>
*<code>[[dom/properties/controlRange|controlRange]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}