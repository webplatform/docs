{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|A mono, stereo, or 4-channel [[apis/webaudio/AudioBuffer|'''AudioBuffer''']] containing the (possibly multi-channel) impulse response used by the [[apis/webaudio/ConvolverNode|'''ConvolverNode''']]. At the time when this attribute is set, the buffer and the state of the normalize attribute will be used to configure the [[apis/webaudio/ConvolverNode|'''ConvolverNode''']] with this impulse response having the given normalization.}}
{{API_Object_Property
|Property_applies_to=apis/webaudio/ConvolverNode
|Read_only=No
|Example_object_name=ConvolverNode
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
var convolver = audioCtx.createConvolver();
convolver.buffer = myAudioBuffer;
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