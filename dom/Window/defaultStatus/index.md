{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/Window
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}