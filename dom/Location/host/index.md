{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/location
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example function returns the '''host''' property of the current page location.
|LiveURL=
|Code=
function getHost()
{
    return document.location.host;
}
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''host''' property is the concatenation of the [[dom/properties/hostname|'''hostname''']] and [[dom/properties/port|'''port''']] properties, separated by a colon (hostname:port). When the '''port''' property is '''null''', the '''host''' property is the same as the '''hostname''' property.
The '''host''' property may be set at any time, although it is safer to set the [[dom/properties/href|'''href''']] property to change a location. If the specified host cannot be found, an error is returned.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
*<code>area</code>
*<code>[[dom/location|location]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}