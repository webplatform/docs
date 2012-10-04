{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=xmlSource|Data type=BSTR|Description=A string that contains serialized XML source code.|Optional=}}
{{Method Parameter|Name=mimeType|Data type=BSTR|Description=A string that identifies one of the following mime types for the source.|Optional=}}
|Method_applies_to=apis/xhr/events/load
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''IHTMLDocument2'''

A document object that represents the DOM tree of the XML source.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
To use the '''parseFromString''' method, type the following syntax.
 <code>oParser {{=}}  new DOMParser();
 oDocument {{=}} oParser.parseFromString(xmlSource, mimeType);</code>
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/xhr/objects/DOMParser|DOMParser]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}