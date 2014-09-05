{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Not implemented and not specified anywhere; deletion candidate.
|Checked_Out=No
|High-level issues=Deletion Candidate, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Not implemented anywhere. Non standard.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=
|Name=selector
|Data type=String
|Description=A page selector.
|Optional=No
}}{{Method Parameter
|Index=
|Name=style
|Data type=String
|Description=This style takes the same form as an inline style specification. For example, "<code>color:blue</code>" is a valid style parameter.
|Optional=No
}}{{Method Parameter
|Index=
|Name=index
|Data type=Number
|Description=The zero-based position in the 	[[css/cssom/pages|'''pages''']] collection where the new [[css/cssom/page|'''page''']] object should be placed.
|Optional=No
}}
|Method_applies_to=css/cssom/styleSheet
|Example_object_name=stylesheet
|Return_value_name=number
|Javascript_data_type=Number
|Return_value_description=Always returns -1.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=
|Notes=Each [[css/cssom/page|'''page''']] object represents a style sheet that corresponds to a '''@page''' rule in the document.
|Import_Notes=
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
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/styleSheet|styleSheet]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}