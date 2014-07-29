{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs createUIEvent example????
don't know why you would specify a different window to the current in creteUIEvent.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Gets the '''window''' object that an event is generated from.
[object window]
}}
{{API_Object_Property
|Property_applies_to=dom/UIEvent
|Read_only=Yes
|Example_object_name=event
|Return_value_name=eventWindow
|Javascript_data_type=DOM Node
|Return_value_description=The window object on which the event occurred.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=Use this property to determine the window object on which the event has occurred.
|Notes=Use [[dom/UIEvent/initUIEvent|initUIEvent]] to set the value of this property.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Events
|URL=http://www.w3.org/TR/DOM-Level-3-Events/
|Status=Working Draft
|Relevant_changes=Section 5.2.1
}}
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/event.view event.view]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974803(v=vs.85).aspx view Property]
|HTML5Rocks_link=
}}