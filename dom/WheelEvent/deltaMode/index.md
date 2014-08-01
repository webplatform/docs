{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs example with difference between MouseWheelEvent and WheelEvent
|Checked_Out=Yes
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Gets a value that indicates the unit of measurement for delta values.}}
{{API_Object_Property
|Property_applies_to=dom/WheelEvent
|Read_only=Yes
|Example_object_name=event
|Return_value_name=deltaMode
|Javascript_data_type=Number
|Return_value_description=One of the following values -
*[[dom/WheelEvent|WheelEvent]].DOM_DELTA_PIXEL, or 0x00 (hex), or 0. The delta coordinates are pixel based (most common).
*[[dom/WheelEvent|WheelEvent]].DOM_DELTA_LINE, or 0x01 (hex), or 1. The delta coordinates are line based (in form controls, for example).
*[[dom/WheelEvent|WheelEvent]].DOM_DELTA_PAGE, or 0x02 (hex), or 2. The delta coordinates are page based.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Events
|URL=http://www.w3.org/TR/DOM-Level-3-Events/
|Status=Working Draft
|Relevant_changes=Section 5.2.4
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/WheelEvent WheelEvent]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974798(v=vs.85).aspx deltaMode Property]
|HTML5Rocks_link=
}}