{{Page_Title|document.write}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections
|Content=Incomplete, Compatibility Incomplete
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Method to insert a string of marked up text in the document tree.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=str
|Data type=String
|Description=A '''String''' that specifies the text and HTML tags to write.
|Optional=No
}}
|Method_applies_to=dom/document
|Example_object_name=document
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=Do not use the '''write''' method or the [[dom/methods/writeln|'''writeln''']] method on the current document after the document has finished loading unless you first call the [[dom/methods/open (document)|'''open''']] method, which clears the current document window and erases all variables.

|Notes=When [[dom/document|'''document''']].'''write''' or '''document'''.[[dom/methods/writeln|'''writeln''']] is used in an event handler, you must also use '''document'''.[[dom/methods/close (document)|'''close''']].
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM HTML Level 2
|URL=http://www.w3.org/TR/DOM-Level-2-HTML/html.html#ID-75233634
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages===
*<code>[[dom/document|document]]</code>
*<code>[[dom/methods/writeln|writeln]]</code>
*<code>[[dom/methods/open (document)|open]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}