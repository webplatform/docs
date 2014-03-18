{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Queries the state of the specified modifier key.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=modifierKeyName
|Data type=String
|Description=One of the following values -
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
}}
|Method_applies_to=dom/KeyboardEvent
|Example_object_name=event
|Return_value_name=modifierState
|Javascript_data_type=Boolean
|Return_value_description=Whether the modifier key is active.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=Some keyboard configurations contain a left and right modifier key. To determine whether the left or right key is pressed, use the  [[dom/KeyboardEvent/location|'''location''']] property.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Events
|URL=http://www.w3.org/TR/DOM-Level-3-Events/
|Status=Working Draft
|Relevant_changes=Section 5.2.6
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