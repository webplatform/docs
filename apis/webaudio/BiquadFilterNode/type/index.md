{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|The type of [[apis/webaudio/BiquadFilterNode|'''BiquadFilterNode''']] (filtering algorithm) the node is implementing.}}
{{API_Object_Property
|Property_applies_to=apis/webaudio/BiquadFilterNode
|Read_only=No
|Example_object_name=BiquadFilterNode
|Return_value_name=
|Javascript_data_type=unsigned short
|Return_value_description=Uses one of the following constant values: 
*LOWPASS (0) (default), a standard second-order resonant lowpass filter with 12dB/octave rolloff; 
*HIGHPASS (1), a standard second-order resonant highpass filter with 12dB/octave rolloff; 
*BANDPASS (2), a second-order bandpass filter; 
*LOWSHELF (3), a second-order lowshelf filter; 
*HIGHSHELF (4), a second-order highshelf filter; 
*PEAKING (5), a boost (or attenuation) to a range of frequencies; 
*NOTCH (6), restricting a set of frequencies; 
*ALLPASS (7), a second-order allpass filter.
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var audioCtx = new AudioContext();
var biquadFilter = audioCtx.createBiquadFilter();
biquadfilter.type = 'lowpass';
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