{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''charset''' attribute is used to declare the character encoding of the document.}}
{{Markup_Attribute
|Applies_to=[[dom/HTMLMetaElement|HTMLMetaElement]]
|Property_applies_to=dom/HTMLElement
|Content=The character encoding declaration must be fit within the first 1024 bytes of an HTML file, hence should be the first child in the the head element. Only one such declaration is allowed within a document.

Note that BOM and declaration in the HTTP header take precedence over in-document declaration.

It’s good practice to declare the character encoding inside the document for situations when the document will be used locally with no HTTP header involved, and as a visual cue in the source code.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=<meta charset="utf-8"/>
}}
}}
{{Notes_Section}}
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
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}