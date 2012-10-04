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
|Description=This example function returns true if the current document URL has a '''hash''' value, or false if the document URL does not.
|LiveURL=
|Code=
function hasHash()
{
    if (document.location.hash {{=}}{{=}} "")
        return false;
    return true;
}
}}}}
{{Notes_Section
|Notes=
===Remarks===
If there is no number sign, this property returns an empty string.
This property is useful for moving to a bookmark within a document. Assigning an invalid value does not cause an error.
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