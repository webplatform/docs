{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters=
|Method_applies_to=
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=C++

 a zero-based index value indicating the position of the imported style sheet in the [[css/cssom/imports|'''imports''']] collection.

JavaScript

 a zero-based index value indicating the position of the imported style sheet in the [[css/cssom/imports|'''imports''']] collection.


}}
{{Topics|DOM}}
{{Notes_Section
|Import_Notes=
===Syntax===
===Parameters===
;''sURL'' [in]:'''String''' that specifies the location of the source file for the style sheet.
;''iIndexRequest'' [in, optional]:'''Integer''' that specifies the requested position for the style sheet in the collection. If this value is not given, the style sheet is added to the end of the collection.
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>IHTMLStyleSheet</code>
*<code>[[css/cssom/styleSheet|styleSheet]]</code>
|Topic_clusters=CSSOM
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}