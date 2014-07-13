{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Stub, Needs Flags
|Content=Incomplete, Compatibility Incomplete, Examples Needed
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The normalized pressure of the pointer input in the range of [0,1], where 0 and 1 represent the minimum and maximum pressure the hardware is capable of detecting, respectively.}}
{{API_Object_Property
|Property_applies_to=dom/PointerEvent
|Read_only=Yes
|Example_object_name=event
|Return_value_name=pressure
|Javascript_data_type=double
|Return_value_description=Pressure of the pointer contact in range of 0 to 1.
|Example_value_name=pressure
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following is an example of a pointermove event handler that outputs the value of the event.pressure property to a text field in a form (frmOutput);
|Code=function getPressure(evt){
var theform=document.forms.frmOutput;
theform.txtPressure.value=evt.pressure;
}
}}
}}
{{Notes_Section
|Usage=
Could be used for example to control the hue or opacity of a color of a line or shape as it is drawn on screen using a pointer, other than a mouse.

For hardware that does not support pressure, including but not limited to mouse, the value must be 1 when in the active buttons state and 0 otherwise.
|Notes=Starting with Internet Explorer 11, this property returns a value of 0.5 for active contact (such as mouse button push) and 0 otherwise on hardware that does not support pressure.
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh772360(v=vs.85).aspx pressure Property PointerEvent]
|HTML5Rocks_link=
}}