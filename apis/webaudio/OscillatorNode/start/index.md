{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Schedules a sound to playback at an exact time.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=when
|Data type=Number
|Description=Describes at what time (in seconds) the sound should start playing. It is in the same time coordinate system as [[apis/webaudio/AudioContext/currentTime|'''AudioContext.currentTime''']]. If 0 is passed in for this value or if the value is less than '''currentTime''', then the sound will start playing immediately. start may only be called one time and must be called before stop is called or an exception will be thrown.
|Optional=No
}}
|Method_applies_to=apis/webaudio/OscillatorNode
|Example_object_name=OscillatorNode
|Return_value_name=
|Javascript_data_type=
|Return_value_description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var oscillator = audioCtx.createOscillator();
oscillator.type = 'square';
oscillator.frequency.value = 3000; // value in hertz
oscillator.start(); // start playing immediately
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