{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Mixed}}
{{API_Name}}
{{Summary_Section|Sets or retrieves the default message displayed in the status bar at the bottom of the window. }}
{{API_Object_Property
|Property_applies_to=dom/Window
|Read_only=No
|Example_object_name=window
|Return_value_name=statusMessage
|Javascript_data_type=String
|Return_value_description=The default message to display on the userAgents' Status Bar.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example displays 'Welcome to our website' in the userAgent's Status Bar when the page loads.
|Code=window.onload=function(){
window.defaultStatus='Welcome to our website!';

};
}}
}}
{{Notes_Section
|Usage=Use to customize the userAgent default Status Bar message.
|Notes====Remarks===
Do not confuse '''defaultStatus''' with [[dom/Window/status|'''status''']]. The '''status''' property reflects a priority or transient message in the status bar, such as the message that appears when an [[dom/MouseEvent/mouseover|'''onmouseover''']] event occurs over an anchor.
Windows Internet Explorer 7: References to this property are ignored if the "Allow status bar updates via script" option is disabled or the URLACTION _FEATURE_SCRIPT_STATUS_BAR URL action is disallowed for the current URL security zone.  For more information on URL security zones, please see About URL Security Zones.

====defaultStatus in Metro style apps using JavaScript====
Metro style apps using JavaScript don't support this property because they  don't have status bars.
|Import_Notes====Syntax===
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Window.defaultStatus defaultStatus]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms533717(v=vs.85).aspx defaultStatus Property]
|HTML5Rocks_link=
}}