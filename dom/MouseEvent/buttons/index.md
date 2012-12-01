{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Gets a value that indicates which mouse buttons a user pressed.}}
{{API_Object_Property
|Property_applies_to=dom/objects/MouseEvent
|Read_only=Yes
|Example_object_name=event
|Return_value_name=pressedButtons
|Javascript_data_type=unsigned short
|Return_value_description=A bitmask that represents the pressed mouse buttons.
*0 - No button.
*1 - The primary button (usually the left mouse button).
*2 - The auxiliary button (usually the middle/wheel mouse button).
*4 - The secondary button (usually the right mouse button).
Other values are always expressed as a power of 2, like 8, 16, 32 and so on and represent other buttons.
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
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=8 and earlier
|Note=A close proprietary alternative for this property is the [[dom/properties/which|which]] property.
}}
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/objects/DragEvent|DragEvent]]</code>
*<code>[[dom/objects/MouseEvent|MouseEvent]]</code>
*<code>[[dom/objects/MouseWheelEvent|MouseWheelEvent]]</code>
*<code>[[dom/objects/WheelEvent|WheelEvent]]</code>
*<code>[[dom/properties/button|button]]</code>
}}
{{Topics|DOM, DOMEvents}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}