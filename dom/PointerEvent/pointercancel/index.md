{{Page_Title}}
{{Flags
|High-level issues=Needs Flags
|Content=Incomplete, Compatibility Incomplete, Examples Needed
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Dispatched when either (1) the user agent has determined that a pointer is unlikely to continue to produce events (e.g., due to a hardware event), or (2) after having fired the [[dom/objects/PointerEvent/pointerdown|pointerdown]] event, the pointer is subsequently used to manipulate the page viewport (e.g., panning or zooming).}}
{{Event
|Event_applies_to=dom/Element
|Content=A user agent will also fire a [[dom/objects/PointerEvent/pointerout|pointerout]] event after firing the pointercancel event.
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
|Usage=This event occurs when the pointer (touch or pen contact) is removed from the system. Here are common reasons why this might happen:
* A touch contact is canceled by a pen coming into range of the surface. 
* The device doesn't report an active contact for more than 100ms.
* A mapping for a device's monitor changes while contacts are active. For example, the user changes the position of a screen in a two screen configuration. 
* The desktop is locked or the user logged off. 
* The number of simultaneous contacts exceeds the number that the device can support. For example, if a device supports only two contact points, if the user has two fingers on a surface, and then touches it with a third finger, this event is raised.
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
|Note=Supported as: [http://msdn.microsoft.com/en-us/library/ie/hh846776(v=vs.85).aspx MSPointerCancel]
}}
}}
{{See_Also_Section
|Topic_clusters=Pointer Events
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/library/ie/hh846776.aspx
|HTML5Rocks_link=
}}