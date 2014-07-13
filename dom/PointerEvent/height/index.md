{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Stub, Needs Flags
|Content=Incomplete, Compatibility Incomplete
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The height (magnitude on the Y axis), in CSS pixels, of the contact geometry of the pointer.}}
{{API_Object_Property
|Property_applies_to=dom/PointerEvent
|Read_only=Yes
|Example_object_name=event
|Javascript_data_type=unsigned long
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Resizing an element to match the contact geometry
|Code=<div style="position:absolute; top:0px; left:0px; width:100px;height:100px;"></div>
<script>
window.addEventListener("pointerdown", checkPointerSize, false);
function checkPointerSize(event) {
	event.target.style.width = event.width + "px";
	event.target.style.height = event.height + "px";
}
</script>
}}
}}
{{Notes_Section
|Usage=This value may be updated on each event for a given pointer. For devices which have a contact geometry but the actual geometry is not reported by the hardware, a default value may be provided by the user agent to approximate the geometry typical of that pointer type. Otherwise, the value must be 0.
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
|Note=Pointer events are supported with the MS prefix. In the example above, IE10 would require '''MSPointerDown'' rather than ''pointerdown''.
}}
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/dn255064(v=vs.85).aspx height Property - PointerEvent]
|HTML5Rocks_link=
}}