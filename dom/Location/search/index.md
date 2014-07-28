{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=compatibility, standards
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets or retrieves the substring of the '''href''' property that follows the question mark.}}
{{API_Object_Property
|Property_applies_to=dom/Location
|Read_only=No
|Example_object_name=location
|Return_value_name=queryString
|Javascript_data_type=String
|Return_value_description=The query string component of the URL.
|Example_value_name=queryString
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example function returns the '''search''' property of the current page location.
|Code=function getSearch() {
    return document.location.search;
}
}}
}}
{{Notes_Section
|Notes=The substring that follows the question mark is the query string or form data.
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