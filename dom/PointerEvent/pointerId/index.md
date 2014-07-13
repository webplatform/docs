{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Stub, Needs Flags
|Content=Incomplete, Compatibility Incomplete, Examples Needed
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|A unique identifier for the pointer causing the event}}
{{API_Object_Property
|Property_applies_to=dom/PointerEvent
|Read_only=Yes
|Example_object_name=event
|Javascript_data_type=unsigned long
|Return_value_description=The unique identifier of the contact for a touch, mouse or pen.
|Example_value_name=lid
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=//  Adds a pointer to the MSGesture object for the red square
function redListener(evt)
{
    if (evt.type == "pointerdown")
    {
        redGesture.addPointer(evt.pointerId);
        return;
    }
    printEvent(evt);
}


}}
}}
{{Notes_Section
|Usage=This identifier must be unique from all other active pointers at the time. A user agent may recycle previously retired values for pointerId from previous active pointers, if necessary.

If the device producing the event is a mouse, then the pointerId must be 1. Device types other than mouse must not have a pointerId of 1.
}}
{{Related_Specifications_Section
|Specifications=
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh772358(v=vs.85).aspx pointerId Property]
|HTML5Rocks_link=
}}