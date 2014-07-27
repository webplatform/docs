{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=More description, compatibility
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets or retrieves the subsection of the '''href''' property that follows the number sign (#).}}
{{API_Object_Property
|Property_applies_to=dom/Location
|Read_only=No
|Example_object_name=location
|Return_value_name=hash
|Javascript_data_type=String
|Return_value_description=The hash component of the URL.
|Example_value_name=hash
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example function returns true if the current document URL has a '''hash''' value, or false if the document URL does not.
|Code=function hasHash() {
    if (document.location.hash {{=}}{{=}}{{=}} "") {
        return false;
    }
    return true;
}
}}
}}
{{Notes_Section
|Notes=If there is no number sign, this property returns an empty string.
This property is useful for moving to a bookmark within a document. Assigning an invalid value does not cause an error.
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}