{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=eventType
|Data type=String
|Description=The name of the event. Sets the value for the [[dom/properties/type (event)|'''type''']] property.
|Optional=No
}}{{Method Parameter
|Name=canBubble
|Data type=Boolean
|Description=Whether the event propagates upward. Sets the value for the [[dom/properties/bubbles|bubbles]] property.
|Optional=No
}}{{Method Parameter
|Name=cancelable
|Data type=Boolean
|Description=Whether the event is cancelable and so [[dom/methods/preventDefault|preventDefault]] can be called. Sets the value for the [[dom/properties/cancelable|cancelable]] property.
|Optional=No
}}{{Method Parameter
|Name=view
|Data type=Object
|Description=The window on which this event is occurring.  Sets the value for the [[dom/properties/view|view]] property.
|Optional=No
}}{{Method Parameter
|Name=detail
|Data type=Number
|Description=Specifies additional information. This value is returned in the [[dom/properties/detail|'''detail''']] property  of the event.
|Optional=No
}}{{Method Parameter
|Name=screenX
|Data type=Number
|Description=The x-coordinate of the mouse pointer, relative to the  upper-left corner of the screen. Sets the value for the [[dom/properties/screenX|'''screenX''']] property,
|Optional=No
}}{{Method Parameter
|Name=screenY
|Data type=Number
|Description=The y-coordinate of the mouse pointer, relative to the  upper-left corner of the screen. Sets the value for the [[dom/properties/screenY|'''screenY''']] property.
|Optional=No
}}{{Method Parameter
|Name=clientX
|Data type=Number
|Description=The x-coordinate of the mouse pointer, relative to the  upper-left corner of the browser's client area. Sets the value for the [[dom/properties/clientX|'''clientX''']] property.
|Optional=No
}}{{Method Parameter
|Name=clientY
|Data type=any
|Description=The y-coordinate of the mouse pointer, relative to the  upper-left corner of the browser's client area. Sets the value for the [[dom/properties/clientY|'''clientY''']] property.
|Optional=No
}}{{Method Parameter
|Name=button
|Data type=Number
|Description=The mouse button that caused the event. Sets the value for the [[dom/properties/button|'''button''']] property (see the property page for common values).
|Optional=No
}}{{Method Parameter
|Name=relatedTarget
|Data type=DOM Node
|Description=A secondary element that is involved in the event. Sets the value for the [[dom/properties/relatedTarget|'''relatedTarget''']] property.
|Optional=No
}}{{Method Parameter
|Name=modifiersListArg
|Data type=String
|Description=A space-separated list of any of the following values:
*'''Alt''' - The left or right Alt key. 
*'''AltGraph''' - The Ctrl and Alt keys.
*'''CapsLock''' - The Caps Lock toggle.
*'''Control''' - The left or right Ctrl key.
*'''Meta''' - The Meta/Control key.
*'''NumLock''' - The Num Lock toggle.
*'''ScrollLock''' - The Scroll Lock toggle.
*'''Shift''' - The left or right Shift key.
*'''Fn'''
*'''OS'''
*'''SymbolLock'''

Other implementation specific options may be supported.
For example -
*'''Win''' (on Microsoft Windows) - The left or right Windows logo key.
*'''Scroll''' - The Scroll Lock toggle.
|Optional=No
}}{{Method Parameter
|Name=deltaX
|Data type=Number
|Description=The distance that the mouse wheel has rotated around the x-axis. Sets the value for the [[dom/properties/deltaX|'''deltaX''']] property.
|Optional=No
}}{{Method Parameter
|Name=deltaY
|Data type=Number
|Description=The distance that the mouse wheel has rotated around the y-axis. Sets the value for the [[dom/properties/deltaY|'''deltaY''']] property.
|Optional=No
}}{{Method Parameter
|Name=deltaZ
|Data type=Number
|Description=The distance that the mouse wheel has rotated around the z-axis. Sets the value for the [[dom/properties/deltaZ|'''deltaZ''']] property.
|Optional=No
}}{{Method Parameter
|Name=deltaMode
|Data type=Number
|Description=The delta mode of the event. Sets the value for the [[dom/properties/deltaMode|'''deltaMode''']] property (see the property page for common values).
|Optional=No
}}
|Method_applies_to=dom/objects/WheelEvent
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
{{Topics|DOM, DOMEvents}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}