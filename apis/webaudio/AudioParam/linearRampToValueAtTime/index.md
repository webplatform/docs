{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Schedules a linear continuous change in parameter value from the previous scheduled parameter value to the given value.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=value
|Data type=Number
|Description=The value the parameter will linearly ramp to at the given time.
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
|Return_value_name=
|Javascript_data_type=
|Return_value_description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var gainNode = audioCtx.createGain();
gainNode.gain.linearRampToValueAtTime(1.0, audioCtx.currentTime + 2); //'gain' is the AudioParam
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Web Audio API
|URL=http://webaudio.github.io/web-audio-api/
|Status=W3C Editor's Draft
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|API, WebAudio}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}