{{Page_Title}}
{{Flags
|High-level issues=Stub, Needs Flags
|Content=Incomplete, Compatibility Incomplete, Examples Needed
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Dispatched when a pointing device is moved into the hit test boundaries of an element or one of its descendants, including as a result of a [[dom/objects/PointerEvent/pointerdown|pointerdown]] event from a device that does not support hover.}}
{{Event
|Event_applies_to=dom/objects/PointerEvent
|Content=This event type is similar to [[dom/objects/PointerEvent/pointerover|pointerover]], but differs in that it does not bubble.
|Interface=dom/objects/PointerEvent
|Target=dom/Element
|Default_action=Varies: when the pointer is primary, all default actions of the [[dom/events/mouseenter|mouseenter]] event
|Synchronous=Yes
|Bubbles=No
|Cancelable=Yes
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=There are similarities between this event type, the [[dom/events/mouseenter|mouseenter]] event described in [http://www.w3.org/TR/DOM-Level-3-Events/ DOM Level 3 Events] and the CSS :hover pseudo-class described in [http://www.w3.org/TR/CSS2/ CSS 2.1]. See also the [[dom/objects/PointerEvent/pointerleave|pointerleave]] event.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Pointer Events
|URL=http://www.w3.org/TR/pointerevents
|Status=Working Draft
|Relevant_changes=3.2.8
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections=Feature Detection
* [[dom/navigator/pointerEnabled|pointerEnabled]]
* [[dom/navigator/maxTouchPoints|maxTouchPoints]]

Events
* [[dom/events/gotpointercapture|gotpointercapture]]
* [[dom/events/lostpointercapture|lostpointercapture]]
* [[dom/events/pointercancel|pointercancel]]
* [[dom/events/pointerdown|pointerdown]]
* [[dom/events/pointerleave|pointerleave]]
* [[dom/events/pointermove|pointermove]]
* [[dom/events/pointerout|pointerout]]
* [[dom/events/pointerover|pointerover]]
* [[dom/events/pointerup|pointerup]]

Objects
* [[dom/objects/PointerEvent|PointerEvent]]

Methods
* [[dom/methods/setPointerCapture|setPointerCapture]]
* [[dom/methods/releasePointerCapture|releasePointerCapture]]

CSS Properties
* [[css/properties/touch-action|touch-action]]
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}