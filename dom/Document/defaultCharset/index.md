{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs a note that this is not a W3C standard and does not work in most browsers, also needs compat table
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Gets the default character set from the current regional language settings.}}
{{API_Object_Property
|Property_applies_to=dom/Document
|Read_only=Yes
|Example_object_name=document
|Return_value_name=defaultCharacterSet
|Javascript_data_type=String
|Return_value_description=The name of the default character set of the user.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=//displays the document's default character encoding string
function showDefCharSet() {
    alert(document.defaultCharset);
}
}}
}}
{{Notes_Section
|Notes=The value depends on the current regional language settings. For typical settings in North America, the value is <code>windows-1252</code>.
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