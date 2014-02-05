{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Initializes a new [[dom/FocusEvent|FocusEvent]] that the  [[dom/Document/createEvent|createEvent]] method created.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=eventType
|Data type=String
|Description=The name of the event. Sets the value for the [[dom/Event/type|'''type''']] property.
|Optional=No
}}{{Method Parameter
|Name=canBubble
|Data type=Boolean
|Description=Whether the event propagates upward. Sets the value for the [[dom/Event/bubbles|bubbles]] property.
|Optional=No
}}{{Method Parameter
|Name=cancelable
|Data type=Boolean
|Description=Whether the event is cancelable and so [[dom/Event/preventDefault|preventDefault]] can be called. Sets the value for the [[dom/Event/cancelable|cancelable]] property.
|Optional=No
}}{{Method Parameter
|Name=view
|Data type=Object
|Description=The window on which this event is occurring.  Sets the value for the [[dom/UIEvent/view|view]] property.
|Optional=No
}}{{Method Parameter
|Name=detail
|Data type=Number
|Description=Specifies additional information. This value is returned in the [[dom/UIEvent/detail|'''detail''']] property of the event.
|Optional=No
}}{{Method Parameter
|Name=relatedTarget
|Data type=DOM Node
|Description=A secondary element that is involved in the event. This value is returned in the [[dom/MouseEvent/relatedTarget|'''relatedTarget''']] property of the event.
|Optional=No
}}
|Method_applies_to=dom/FocusEvent
|Example_object_name=event
|Javascript_data_type=void
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
|Relevant_changes=Section 5.2.2
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/FocusEvent|FocusEvent]]</code>
*<code>[[dom/UIEvent/initUIEvent|initUIEvent]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}