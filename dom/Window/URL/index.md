{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=should be document.URL not window>URL

|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Sets or gets the URL for the current document.}}
{{API_Object_Property
|Property_applies_to=dom/Window
|Read_only=No
|Example_object_name=document
|Return_value_name=string
|Javascript_data_type=String
|Return_value_description=the URL of the current web document.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example function returns the '''URL''' property of the current document.
|Code=function getURL()
{
    return document.URL;
}
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''URL''' property is case-sensitive.
This property is an alias for the [[dom/Location|'''location''']].[[dom/Location/href|'''href''']] property on the window.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.4
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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/document.URL document.URL]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms534708(v=vs.85).aspx URL Property]
|HTML5Rocks_link=
}}