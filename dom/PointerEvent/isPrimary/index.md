{{Page_Title}}
{{Flags
|High-level issues=Stub
|Content=Incomplete, Compatibility Incomplete, Examples Needed
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Indicates if the pointer represents the primary pointer.}}
{{API_Object_Property
|Property_applies_to=dom/PointerEvent
|Read_only=Yes
|Example_object_name=event
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=In a multi-pointer (e.g. multi-touch) scenario, the primary pointer is used to identify a master pointer amongst the set of active pointers. This pointer is the one that will produce compatibility mouse events. It is also useful when single-pointer interaction is desired by an author.

When dispatching a pointer event, a pointer is considered primary if: 
* The pointer represents a mouse device.
* The pointer represents ''primary touch input'', where its pointerdown event was dispatched when no other active pointers representing touch input existed.
* The pointer represents ''primary pen input'', where its pointerdown event was dispatched when no other active pointers representing pen input existed.
|Notes=In some platforms, the primary pointer is determined using all active pointers on the device including those not targeted at the user agent (e.g. in another application). This means it is possible for the user agent to fire pointer events in which no pointer is marked as the primary pointer. For example, if the first touch interaction is targeted outside the user agent and a secondary (multi-touch) touch interaction is targeted inside the user agent, then the user agent fires pointer events for the second contact with a value of false for isPrimary.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Pointer Events
|URL=http://www.w3.org/TR/pointerevents
|Status=Working Draft
|Relevant_changes=3.1.2
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
|Internet_explorer_supported=Yes
|Internet_explorer_version=IE10
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
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
|Note=The PointerEvent object and associated events are supported with the MS prefix. E.g., [http://msdn.microsoft.com/en-us/library/ie/hh772103(v=vs.85).aspx MSPointerEvent]
}}
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}