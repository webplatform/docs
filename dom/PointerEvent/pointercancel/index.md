{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Flags
|Content=Incomplete, Compatibility Incomplete, Examples Needed
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Dispatched when either (1) the user agent has determined that a pointer is unlikely to continue to produce events (e.g., due to a hardware event), or (2) after having fired the [[dom/PointerEvent/pointerdown|pointerdown]] event, the pointer is subsequently used to manipulate the page viewport (e.g., panning or zooming).}}
{{Event
|Event_applies_to=dom/PointerEvent
|Synchronous=Yes
|Bubbles=Yes
|Target=dom/Element
|Cancelable=Yes
|Default_action=None
|Content=A user agent will also fire a [[dom/PointerEvent/pointerout|pointerout]] event after firing the pointercancel event.
|Interface=dom/PointerEvent
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=element.addEventListener("pointercancel", handler, useCapture) ;
}}
}}
{{Notes_Section
|Usage=This event occurs when the pointer (touch or pen contact) is removed from the system. Here are common reasons why this might happen:
* A touch contact is canceled by a pen coming into range of the surface. 
* The device doesn't report an active contact for more than 100ms.
* A mapping for a device's monitor changes while contacts are active. For example, the user changes the position of a screen in a two screen configuration. 
* The desktop is locked or the user logged off. 
* The number of simultaneous contacts exceeds the number that the device can support. For example, if a device supports only two contact points, if the user has two fingers on a surface, and then touches it with a third finger, this event is raised.
|Notes=When the pointercancel event is raised for a pointer, the app won’t receive any other events for that pointer, including pointerup . The app should perform any necessary cleanup as required for the pointer. For example, if the app maintains a pointer list, the app should remove the pointer from the list. 

You shouldn't treat this event like an pointerup event. When a pointer is removed, the app should cancel any ongoing work. The following example shows how you might handle pointer events if the target is a button:

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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh846776(v=vs.85).aspx pointercancel Event]
|HTML5Rocks_link=
}}