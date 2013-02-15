{{Page_Title}}
{{Flags
|High-level issues=Stub, Needs Flags
|Content=Incomplete, Compatibility Incomplete, Examples Needed
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Dispatched when either (1) the user agent has determined that a pointer is unlikely to continue to produce events (e.g., due to a hardware event), or (2) after having fired the [[dom/objects/PointerEvent/pointerdown|pointerdown]] event, the pointer is subsequently used to manipulate the page viewport (e.g., panning or zooming).}}
{{Event
|Event_applies_to=dom/objects/PointerEvent
|Content=A user agent must also fire a [[dom/objects/PointerEvent/pointerout|pointerout]] event after firing the pointercancel event.
|Interface=dom/objects/PointerEvent
|Target=dom/Element
|Default_action=None
|Synchronous=Yes
|Bubbles=Yes
|Cancelable=Yes
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=Examples of scenarios in which a user agent might determine that a pointer is unlikely to continue to produce events include:
* A device's screen orientation is changed while a pointer is active.
* The user inputs a greater number of simultaneous pointers than is supported by the device
* The user agent interprets the input as accidental (for example, the hardware supports palm rejection).
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Pointer Events
|URL=http://www.w3.org/TR/pointerevents
|Status=Working Draft
|Relevant_changes=3.2.4
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