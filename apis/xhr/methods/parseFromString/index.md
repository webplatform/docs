{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=xmlSource
|Data type=BSTR
|Description=A string that contains serialized XML source code.
|Optional=No
}}{{Method Parameter
|Index=1
|Name=mimeType
|Data type=BSTR
|Description=A string that identifies one of the following mime types for the source.
|Optional=No
}}
|Method_applies_to=apis/xhr/events/load
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''IHTMLDocument2'''

A document object that represents the DOM tree of the XML source.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=To use the '''parseFromString''' method, type the following syntax.
|Code=oParser {{=}}  new DOMParser();
oDocument {{=}} oParser.parseFromString(xmlSource, mimeType);
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[[apis/xhr/objects/DOMParser|DOMParser]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}