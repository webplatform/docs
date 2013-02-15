{{Page_Title}}
{{Flags
|High-level issues=Stub, Needs Flags
|Content=Incomplete, Compatibility Incomplete, Examples Needed
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Dispatched when a pointer enters the state of having a non-zero value for the buttons property. }}
{{Event
|Event_applies_to=dom/objects/PointerEvent
|Content=For mouse, this is when the device has at least one button depressed. For touch, this is when there is physical contact with the digitizer. For pen, this is when the pen has physical contact with the digitizer.

For input devices that do not support hover, the user agent also fires a pointerover event preceding the pointerdown event.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=For mouse (or other multi-button pointer devices), this means pointerdown and pointerup are dispatched differently than mousedown and mouseup.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Pointer Events
|URL=http://www.w3.org/TR/pointerevents
|Status=Working Draft
|Relevant_changes=3.2.2
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