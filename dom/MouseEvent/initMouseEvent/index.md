{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Initializes a new mouse event that the  [[dom/Document/createEvent|'''createEvent''']] method created.}}
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
|Data type=DOM Node
|Description=The window on which this event is occurring. Sets the value for the [[dom/UIEvent/view|view]] property.
|Optional=No
}}{{Method Parameter
|Name=detail
|Data type=Number
|Description=Specifies additional information. This value is returned in the [[dom/UIEvent/detail|'''detail''']] property  of the event.
|Optional=No
}}{{Method Parameter
|Name=screenX
|Data type=Number
|Description=The x-coordinate of the mouse pointer, relative to the  upper-left corner of the screen. Sets the value for the [[dom/MouseEvent/screenX|'''screenX''']] property,
|Optional=No
}}{{Method Parameter
|Name=screenY
|Data type=Number
|Description=The y-coordinate of the mouse pointer, relative to the  upper-left corner of the screen. Sets the value for the [[dom/MouseEvent/screenY|'''screenY''']] property.
|Optional=No
}}{{Method Parameter
|Name=clientX
|Data type=Number
|Description=The x-coordinate of the mouse pointer, relative to the  upper-left corner of the browser's client area. Sets the value for the [[dom/MouseEvent/clientX|'''clientX''']] property.
|Optional=No
}}{{Method Parameter
|Name=clientY
|Data type=Number
|Description=The y-coordinate of the mouse pointer, relative to the  upper-left corner of the browser's client area. Sets the value for the [[dom/MouseEvent/clientY|'''clientY''']] property.
|Optional=No
}}{{Method Parameter
|Name=ctrlKey
|Data type=Boolean
|Description=Whether the Control key is depressed. Sets the value for the [[dom/KeyboardEvent/ctrlKey|'''ctrlKey''']] property.
|Optional=No
}}{{Method Parameter
|Name=altKey
|Data type=Boolean
|Description=Whether the Alt key is depressed. Sets the value for the [[dom/KeyboardEvent/altKey|'''altKey''']] property.
|Optional=No
}}{{Method Parameter
|Name=shiftKey
|Data type=Boolean
|Description=Whether the Shift key is depressed. Sets the value for the [[dom/KeyboardEvent/shiftKey|'''shiftKey''']] property.
|Optional=No
}}{{Method Parameter
|Name=metaKey
|Data type=Boolean
|Description=Whether a meta key is depressed. Sets the value for the [[dom/KeyboardEvent/metaKey|'''metaKey''']] property.
|Optional=No
}}{{Method Parameter
|Name=button
|Data type=Number
|Description=The mouse button that caused the event. Sets the value for the [[dom/MouseEvent/button|'''button''']] property (see the property page for common values).
|Optional=No
}}{{Method Parameter
|Name=relatedTarget
|Data type=DOM Node
|Description=A secondary element that is involved in the event.  Sets the value for the [[dom/MouseEvent/relatedTarget|'''relatedTarget''']] property.
|Optional=No
}}
|Method_applies_to=dom/MouseEvent
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
|Relevant_changes=Section 5.2.3
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
{{Topics|DOM, DOMEvents}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}