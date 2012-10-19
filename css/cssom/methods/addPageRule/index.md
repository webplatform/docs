{{Page_Title|Not implemented anywhere - ignore}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Not implemented anywhere. Non standard.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=selector
|Data type=String
|Description=A page selector.
|Optional=No
}}{{Method Parameter
|Name=style
|Data type=String
|Description=This style takes the same form as an inline style specification. For example, "<code>color:blue</code>" is a valid style parameter.
|Optional=No
}}{{Method Parameter
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
|Notes=Each [[css/cssom/page|'''page''']] object represents a style sheet that corresponds to a '''@page''' rule in the document.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSSOM
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