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