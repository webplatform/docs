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
|Name=psarray
|Data type=any
|Description=A '''String''' that specifies the text and HTML tags to write.
|Optional=No
}}
|Method_applies_to=dom/Document
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
In HTML, the carriage return is ignored unless it occurs in preformatted text.
Do not use the [[dom/Document/write|'''write''']] method or the '''writeln''' method on the current document after the document has finished loading unless you first call the [[dom/Document/open|'''open''']] method, which clears the current document window and erases all variables.
'''Note'''  When [[dom/Document|'''Document''']].[[dom/Document/write|'''write''']] or '''document'''.'''writeln''' is used in an event handler, you must also use '''document'''.[[dom/Document/close|'''close''']].
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.5
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
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>Reference</code>
*<code>[[dom/Document/write|write]]</code>
*<code>[[dom/Document/open|open]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}