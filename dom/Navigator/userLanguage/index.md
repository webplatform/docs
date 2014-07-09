{{Page_Title}}
{{Flags
|State=Unreviewed
|Checked_Out=Yes
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Retrieves the operating system's natural language setting.

This property reflects the setting in the "Your locale (location)" box in the Regional Options of Control Panel—for example, "English (United States).
}}
{{API_Object_Property
|Property_applies_to=dom/Navigator
|Read_only=Yes
|Example_object_name=navigator
|Return_value_name=result
|Javascript_data_type=String
|Return_value_description=see [http://msdn.microsoft.com/en-us/library/ms533052(v=vs.85).aspx Language Codes] for a full listing of possible values.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=Do not use as this property reflects the language preferences of the users' Operating system NOT their language preferences for web content.
|Notes====Remarks===
This property reflects the setting in the "Your locale (location)" box in the Regional Options of Control Panel—for example, "English (United States).
|Import_Notes====Syntax===
var result=navigator.userLanguage;
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms534713(v=vs.85).aspx navigator.userLanguage]
|HTML5Rocks_link=
}}