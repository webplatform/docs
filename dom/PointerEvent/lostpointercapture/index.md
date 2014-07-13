{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs example

|Checked_Out=No
|High-level issues=Stub, Needs Flags
|Content=Incomplete, Compatibility Incomplete, Examples Needed
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Dispatched after pointer capture is released for a pointer.}}
{{Event
|Event_applies_to=dom/PointerEvent
|Synchronous=No
|Bubbles=Yes
|Target=dom/Element
|Cancelable=No
|Default_action=None
|Content=This event is dispatched prior to any subsequent events for the pointer after capture was released. This event is dispatched to the element from which pointer capture was removed. Subsequent events for that pointer follow normal hit testing mechanisms for determining the event target. See [[dom/Element/releasePointerCapture|releasePointerCapture]].
|Interface=dom/PointerEvent
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=Note  As of Internet Explorer 11, the Microsoft vendor prefixed version of this event (MSLostPointerCapture) is no longer supported and may be removed in a future release. Instead, use the non-prefixed lowercase name, lostpointercapture, which is better for standards compliance and future compatibility.
}}
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
|Note=Supported as: [http://msdn.microsoft.com/en-us/library/ie/hh771907(v=vs.85).aspx MSLostPointerCapture]
}}
}}
{{See_Also_Section
|Manual_links=[http://code.msdn.microsoft.com/ie/Pointers-and-Gestures-ae95918f code.MSDN Pointers and Gestures Example]

[http://msdn.microsoft.com/en-us/library/ie/dn433244(v=vs.85).aspx#feature_detection_and_touch_support_testing Feature Detection and Touch Support Testing]

[http://blogs.msdn.com/b/eternalcoding/archive/2013/01/16/hand-js-a-polyfill-for-supporting-pointer-events-on-every-browser.aspx Hand.js - A polyfill for supporting pointer events on every browser.]

[https://github.com/toolkitchen/PointerEvents PointerEvents Polyfill on Github]
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh771907(v=vs.85).aspx lostPointerCapture Event]
|HTML5Rocks_link=
}}