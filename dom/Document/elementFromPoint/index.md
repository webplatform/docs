{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=x
|Data type=Number
|Description=A number that specifies the X-offset, in pixels.
|Optional=No
}}{{Method Parameter
|Name=y
|Data type=Number
|Description=A number that specifies the Y-offset, in pixels.
|Optional=No
}}
|Method_applies_to=dom/document
|Example_object_name=document
|Return_value_name=myElement
|Javascript_data_type=DOM Node
|Return_value_description='''IHTMLElement'''
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
Coordinates are supplied in client coordinates. The upper-left corner of the client area is (0,0). For '''elementFromPoint''' to exhibit expected behavior, the object or element located at position (x, y) must support and respond to mouse events.
|Import_Notes====Syntax===
===Standards information===
There are no standards that apply here.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSSOM View Module
|URL=http://dev.w3.org/csswg/cssom-view/#widl-Document-elementFromPoint-Element-float-x-float-y
|Status=Editor's Draft 3
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
*<code>Reference</code>
*<code>[[dom/properties/clientX2|clientX]]</code>
*<code>[[dom/properties/clientY2|clientY]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}