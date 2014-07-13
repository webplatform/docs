{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Stub, Needs Flags
|Content=Incomplete, Cleanup, Compatibility Incomplete, Examples Needed
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Dispatched when a pointer leaves the state of having a non-zero value for the [[dom/MouseEvent/buttons|buttons]] property.}}
{{Event
|Event_applies_to=dom/PointerEvent
|Synchronous=Yes
|Bubbles=Yes
|Target=dom/Element
|Cancelable=Yes
|Default_action=Varies: when the pointer is primary, all default actions of the [[dom/MouseEvent/mouseup|mouseup]] event
|Content=For mouse, this is when the device transitions from at least one button depressed to no buttons depressed. For touch, this is when physical contact is removed from the digitizer. For pen, this is when the pen is removed from physical contact with the digitizer. 

For input devices that do not support hover, a user agent must also fire a pointerout event after firing the pointerup event.
|Interface=dom/PointerEvent
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=element.addEventListener("pointerup", handler, useCapture) ;
}}
}}
{{Notes_Section
|Notes=Some pointer devices, such as mouse or pen, support multiple buttons. In the [http://www.w3.org/TR/DOM-Level-3-Events/ DOM Level 3 Events] Mouse Event model, each button press produces a mousedown and mouseup event.  

Pointer Events do not fire overlapping pointerdown and pointerup events when an additional button is depressed while another button on the pointer device is already depressed. For detecting these cases, see [http://www.w3.org/TR/pointerevents/#chorded-button-interactions Chorded Button Interactions] in the PointerEvents specification.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Pointer Events
|URL=http://www.w3.org/TR/pointerevents
|Status=Working Draft
|Relevant_changes=3.2.3
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
|Note=Supported as: [http://msdn.microsoft.com/en-us/library/ie/hh771914(v=vs.85).aspx MSPointerUp]
}}
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh771914(v=vs.85).aspx pointerup Event]
|HTML5Rocks_link=
}}