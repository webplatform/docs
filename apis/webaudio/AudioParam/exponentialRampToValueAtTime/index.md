{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs example
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Schedules an exponential continuous change in parameter value from the previous scheduled parameter value to the given value. Parameters representing filter frequencies and playback rate are best changed exponentially because of the way humans perceive sound.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=value
|Data type=Number
|Description=The value the parameter will exponentially ramp to at the given time. An exception will be thrown if this value is less than or equal to 0, or if the value at the time of the previous event is less than or equal to 0.
|Optional=No
}}{{Method Parameter
|Index=1
|Name=endTime
|Data type=Number
|Description=The time in the same time coordinate system as [[apis/webaudio/AudioContext/currentTime|'''AudioContext.currentTime''']].
|Optional=No
}}
|Method_applies_to=apis/webaudio/AudioParam
|Example_object_name=AudioParam
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
{{Topics|API, WebAudio}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}