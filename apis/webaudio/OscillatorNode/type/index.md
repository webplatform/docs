{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|The shape of the periodic waveform. It may directly be set to any of the type constant values except for CUSTOM. The [[apis/webaudio/OscillatorNode/setWaveTable|'''setWaveTable()''']] method can be used to set a custom waveform, which results in this attribute being set to CUSTOM.}}
{{API_Object_Property
|Property_applies_to=apis/webaudio/OscillatorNode
|Read_only=No
|Example_object_name=OscillatorNode
|Return_value_name=
|Javascript_data_type=unsigned short
|Return_value_description=Uses one of the following constant values: 
*SINE (0); 
*SQUARE (1); 
*SAWTOOTH (2); 
*TRIANGLE (3); 
*CUSTOM (4).
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var oscillator = audioCtx.createOscillator();
oscillator.type = 'square';
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