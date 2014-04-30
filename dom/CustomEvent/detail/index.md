{{Page_Title|detail (CustomEvent)}}
{{Flags
|High-level issues=Needs Review
|Content=Examples Needed
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Retrieves additional information about an event.}}
{{API_Object_Property
|Property_applies_to=dom/CustomEvent
|Read_only=Yes
|Example_object_name=event
|Return_value_name=eventDetails
|Return_value_description=The content of this property is user-defined. It can be an integer, date, array, or other object type.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=Use this property to retrieve any available additional information about this developer-generated custom event. Note: It may not contain any information.
|Notes=After a custom event object is created, use the [[dom/CustomEvent/initCustomEvent|initCustomEvent]] method to set the value of the this property.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Events
|URL=http://www.w3.org/TR/DOM-Level-3-Events/
|Status=Working Draft
|Relevant_changes=Section 4.2
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}