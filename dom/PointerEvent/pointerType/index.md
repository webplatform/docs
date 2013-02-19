{{Page_Title}}
{{Flags
|High-level issues=Stub, Needs Flags
|Content=Incomplete, Compatibility Incomplete
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Indicates the device type that caused the event (mouse, pen, touch, etc.).}}
{{API_Object_Property
|Property_applies_to=dom/objects/PointerEvent
|Read_only=Yes
|Example_object_name=event
|Javascript_data_type=String
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Detecting the type of input from a user
|Code=window.addEventListener("pointerdown", detectInputType, false);
function detectInputType(event) {
	switch(event.pointerType) {
		case "mouse":
			alert("You used a mouse!");
			break;
		case "pen":
			alert("You used a pen stylus!");
			break;
		case "touch":
			alert("You used touch!");
			break;	
		default:
			alert("Not sure what device was used!");
	}
}
}}
}}
{{Notes_Section
|Usage=If a user agent is to fire a pointer event for a mouse, pen stylus, or touch input device, then the value of pointerType must be according to the following table:

{{{!}}
! Pointer Device Type
! pointerType Value
{{!}}-
{{!}} Mouse
{{!}} mouse
{{!}}-
{{!}} Pen Stylus
{{!}} pen
{{!}}-
{{!}} Touch Contact
{{!}} touch
{{!}}}

If the device type cannot be detected by the user agent, then the value must be an empty string. If a user agent supports pointer device types other than those listed above, the value of pointerType should be vendor prefixed to avoid conflicting names for different types of devices. Future specifications may provide additional normative values for other device types.
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
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}