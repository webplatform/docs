{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|N/A}}
{{API_Name}}
{{Summary_Section}}
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
|Description=The window on which this event is occurring. Sets the value for the [[dom/IUEvent/view|view]] property.
|Optional=No
}}{{Method Parameter
|Name=data
|Data type=String
|Description=Character data. Sets the value for the [[dom/CompositionEvent/data|'''data''']]  property.
|Optional=No
}}{{Method Parameter
|Name=inputMethod
|Data type=Number
|Description=The input mode for the text. Sets the value for the [[dom/TextEvent/inputMethod|'''inputMethod''']] property.
|Optional=No
}}{{Method Parameter
|Name=locale
|Data type=String
|Description=The locale name. Sets the value for the [[dom/CompositionEvent/locale|'''locale''']] property.
|Optional=No
}}
|Method_applies_to=dom/TextEvent
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
|Name=DOM Level 3 Events (20110531)
|URL=http://www.w3.org/TR/2011/WD-DOM-Level-3-Events-20110531
|Status=Outdated Working Draft
|Relevant_changes=Section 5.2.5
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