{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|An [[apis/webaudio/AudioParam|'''AudioParam''']] object representing the amount of delay (in seconds) to apply. The default value (delayTime.value) is 0 (no delay). The minimum value is 0 and the maximum value is determined by the '''maxDelayTime''' argument to the [[apis/webaudio/AudioContext|'''AudioContext''']] method [[apis/webaudio/AudioContext/createDelay|'''createDelay''']]. This parameter is k-rate.}}
{{API_Object_Property
|Property_applies_to=apis/webaudio/DelayNode
|Read_only=No
|Example_object_name=DelayNode
|Return_value_name=
|Javascript_data_type=
|Return_value_description=
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var audioCtx = new AudioContext();
var myDelay = audioCtx.createDelay(5.0);
myDelay.delayTime.value = 3.0;
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