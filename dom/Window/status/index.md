{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|N/A}}
{{API_Name}}
{{Summary_Section|Sets the text in the status bar at the bottom of the browser or returns the previously set text.}}
{{API_Object_Property
|Property_applies_to=dom/Window
|Read_only=No
|Example_object_name=window
|Return_value_name=message
|Javascript_data_type=String
|Return_value_description=The text contents of the userAgents' Status Bar
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=window.onload{{=}}function(){
window.status='loaded.....';
}
}}
}}
{{Notes_Section
|Notes====Remarks===
|Import_Notes====Syntax===
window.status {{=}} string;
var value {{=}} window.status;
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
|Sources=MDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Window.status status]
|MSDN_link=
|HTML5Rocks_link=
}}