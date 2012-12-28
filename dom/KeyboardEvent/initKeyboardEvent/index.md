{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Initializes a new keyboard event that the  [[dom/methods/createEvent|'''createEvent''']] method created.}}
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
|Name=key
|Data type=Number
|Description=The [[dom/events/apis/constants/key identifiers|'''key identifier''']]. Sets the value for the [[dom/properties/key|'''key''']] property.
|Optional=No
}}{{Method Parameter
|Name=location
|Data type=Number
|Description=The location of the key on the device. Sets the value for the [[dom/properties/location|'''location''']] property.
|Optional=No
}}{{Method Parameter
|Name=modifiersList
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
|Name=repeat
|Data type=Number
|Description=The number of times this key has been pressed. Sets the value for the [[dom/properties/repeat2|'''repeat''']] property.
|Optional=No
}}{{Method Parameter
|Name=locale
|Data type=String
|Description=The locale name. Sets the value for the [[dom/properties/locale|'''locale''']] property.
|Optional=No
}}
|Method_applies_to=dom/objects/KeyboardEvent
|Example_object_name=event
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=The information in this page corresponds to the 20100908 outdated working draft edition of the specifications.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Events (20090908)
|URL=http://www.w3.org/TR/2009/WD-DOM-Level-3-Events-20090908/
|Status=Outdated Working Draft
|Relevant_changes=Section 5.2.7
}}{{Related Specification
|Name=DOM Level 3 Events (20100907)
|URL=http://www.w3.org/TR/2010/WD-DOM-Level-3-Events-20100907/
|Status=Outdated Working Draft
|Relevant_changes=Section 5.2.6
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.10
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Chrome/Safari
|Note=Implement an older draft of the specification (20090908), that is missing the '''locale''' parameter.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=9, 10
|Note=Implements an older draft of the specification (20100907), that is missing the '''char''' parameter.
}}
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