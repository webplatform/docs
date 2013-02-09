{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Creates a [[apis/webaudio/DelayNode|'''DelayNode''']] representing a variable delay line. The initial default delay time will be 0 seconds.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=maxDelayTime
|Data type=Number
|Description=Specifies the maximum delay time in seconds allowed for the delay line. If specified, this value must be greater than zero and less than three minutes or a NOT_SUPPORTED_ERR exception will be thrown.
|Optional=Yes
}}
|Method_applies_to=apis/webaudio/AudioContext
|Example_object_name=AudioContext
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Web Audio API
|URL=https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html
|Status=W3C Editor's Draft
}}
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Audio}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}