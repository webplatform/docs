{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/Window
|Read_only=
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
Do not confuse '''defaultStatus''' with [[dom/properties/status|'''status''']]. The '''status''' property reflects a priority or transient message in the status bar, such as the message that appears when an [[dom/events/mouseover|'''onmouseover''']] event occurs over an anchor.
Windows Internet Explorer 7. References to this property are ignored if the "Allow status bar updates via script" option is disabled or the URLACTION _FEATURE_SCRIPT_STATUS_BAR URL action is disallowed for the current URL security zone.  For more information on URL security zones, please see About URL Security Zones.

====defaultStatus in Metro style apps using JavaScript====
Metro style apps using JavaScript don't support this property because they  don't have status bars.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>window</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}