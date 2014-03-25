{{Page_Title}}
{{Flags
|High-level issues=Stub, Needs Flags
|Content=Compatibility Incomplete, Examples Needed
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Dispatched when any of the following occurs:
* A pointing device is moved out of the hit test boundaries of an element
* After firing the [[dom/PointerEvent/pointerup|pointerup]] event for a device that does not support hover
* After firing the [[dom/PointerEvent/pointercancel|pointercancel]] event
}}
{{Event
|Event_applies_to=dom/PointerEvent
|Synchronous=Yes
|Bubbles=Yes
|Target=dom/Element
|Cancelable=Yes
|Default_action=Varies: when the pointer is primary, all default actions of the [[dom/MouseEvent/mouseout|mouseout]] event
|Interface=dom/objects/PointerEvent
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Pointer Events
|URL=http://www.w3.org/TR/pointerevents
|Status=Working Draft
|Relevant_changes=3.2.7
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Yes
|Internet_explorer_prefixed_version=IE10
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=10
|Note=Supported as: [http://msdn.microsoft.com/en-us/library/ie/hh771912(v=vs.85).aspx MSPointerOut]
}}
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}