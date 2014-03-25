{{Page_Title}}
{{Flags
|High-level issues=Stub, Needs Flags
|Content=Incomplete, Compatibility Incomplete, Examples Needed
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Dispatched when a pointing device is moved off of the hit test boundaries of an element and all of its descendants, including as a result of a [[dom/PointerEvent/pointerup|pointerup]] event from a device that does not support hover.}}
{{Event
|Event_applies_to=dom/PointerEvent
|Synchronous=Yes
|Bubbles=No
|Target=dom/Element
|Cancelable=Yes
|Default_action=Varies: when the pointer is primary, all default actions of the [[dom/MouseEvent/mouseleave|mouseleave]] event.
|Content=This event type is similar to [[dom/PointerEvent/pointerout|pointerout]], but differs in that it does not bubble and that it is not dispatched until the pointing device has left the boundaries of the element and the boundaries of all its children.
|Interface=dom/PointerEvent
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=There are similarities between this event type, the [[dom/MouseEvent/mouseleave|mouseleave]] event described in [http://www.w3.org/TR/DOM-Level-3-Events/ DOM Level 3 Events] and the CSS :hover pseudo-class described in [http://www.w3.org/TR/CSS2/ CSS 2.1]. See also the [[dom/PointerEvent/pointerenter|pointerenter]] event.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Pointer Events
|URL=http://www.w3.org/TR/pointerevents
|Status=Working Draft
|Relevant_changes=3.2.9
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
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}