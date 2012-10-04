{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=psarray|Data type=SAFEARRAY|Description=A '''String''' that specifies the text and HTML tags to write.|Optional=}}
|Method_applies_to=dom/document
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
In HTML, the carriage return is ignored unless it occurs in preformatted text.
Do not use the [[dom/methods/write|'''write''']] method or the '''writeln''' method on the current document after the document has finished loading unless you first call the [[dom/methods/open (document)|'''open''']] method, which clears the current document window and erases all variables.
'''Note'''  When [[dom/document|'''document''']].[[dom/methods/write|'''write''']] or '''document'''.'''writeln''' is used in an event handler, you must also use '''document'''.[[dom/methods/close (document)|'''close''']].
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
*<code>Reference</code>
*<code>[[dom/methods/write|write]]</code>
*<code>[[dom/methods/open (document)|open]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}