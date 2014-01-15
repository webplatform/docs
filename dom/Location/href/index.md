{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets or retrieves the entire URL as a string.}}
{{API_Object_Property
|Property_applies_to=dom/Location
|Read_only=No
|Example_object_name=location
|Return_value_name=url
|Javascript_data_type=String
|Return_value_description=The URL of the document.
|Example_value_name=url
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example shows a URL list. The user is taken to the URL selected from the options, if the selection is different from the list's default value.
|Code=&lt;select onchange{{=}}"window.location.href{{=}}this.options[this.selectedIndex].value"&gt;
&lt;option value{{=}}"http://www.microsoft.com/ie"&gt;Internet Explorer&lt;/option&gt;
&lt;option value{{=}}"http://www.microsoft.com"&gt;Microsoft Home&lt;/option&gt;
&lt;option value{{=}}"http://msdn.microsoft.com"&gt;Developer Network&lt;/option&gt;
&lt;/select&gt;
}}
}}
{{Notes_Section}}
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