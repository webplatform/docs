{{Page_Title}}
{{Flags
|High-level issues=Stub, Needs Flags
|Content=Incomplete, Compatibility Incomplete, Examples Needed
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Dispatched after pointer capture is released for a pointer.}}
{{Event
|Event_applies_to=dom/Element
|Content=This event is dispatched prior to any subsequent events for the pointer after capture was released. This event is dispatched to the element from which pointer capture was removed. Subsequent events for that pointer follow normal hit testing mechanisms for determining the event target. See [[dom/methods/releasePointerCapture|releasePointerCapture]].
|Interface=dom/objects/PointerEvent
|Target=dom/Element
|Default_action=None
|Synchronous=No
|Bubbles=Yes
|Cancelable=No
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Pointer Events
|URL=http://www.w3.org/TR/pointerevents
|Status=Working Draft
|Relevant_changes=3.2.11
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