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
|Data type=String
|Description=A '''Integer''' that specifies the X-offset, in pixels.
|Optional=No
}}{{Method Parameter
|Name=y
|Data type=String
|Description=A '''Integer''' that specifies the Y-offset, in pixels.
|Optional=No
}}
|Method_applies_to=dom/document
|Example_object_name=object
|Return_value_name=object
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
|Desktop_rows=
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