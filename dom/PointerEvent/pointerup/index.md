{{Page_Title}}
{{Flags
|High-level issues=Stub, Needs Flags
|Content=Incomplete, Cleanup, Compatibility Incomplete, Examples Needed
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Dispatched when a pointer leaves the state of having a non-zero value for the [[dom/properties/buttons|buttons]] property.}}
{{Event
|Event_applies_to=dom/objects/PointerEvent
|Content=For mouse, this is when the device transitions from at least one button depressed to no buttons depressed. For touch, this is when physical contact is removed from the digitizer. For pen, this is when the pen is removed from physical contact with the digitizer. 

For input devices that do not support hover, a user agent must also fire a pointerout event after firing the pointerup event.
|Interface=dom/objects/PointerEvent
|Target=dom/Element
|Default_action=Varies: when the pointer is primary, all default actions of the [[dom/events/mouseup|mouseup]] event
|Synchronous=Yes
|Bubbles=Yes
|Cancelable=Yes
}}
{{Examples_Section
|Not_required=No
|Examples=
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
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}