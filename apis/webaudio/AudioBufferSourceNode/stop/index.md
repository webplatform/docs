{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs example, return type
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Schedules a sound to stop playback at an exact time.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=when
|Data type=Number
|Description=Describes at what time (in seconds) the sound should stop playing. It is in the same time coordinate system as [[apis/webaudio/AudioContext/currentTime|'''AudioContext.currentTime''']]. If 0 is passed in for this value or if the value is less than '''currentTime''', then the sound will stop playing immediately. stop must only be called one time and only after a call to start or stop, or an exception will be thrown.
|Optional=No
}}
|Method_applies_to=apis/webaudio/AudioBufferSourceNode
|Example_object_name=AudioBufferSourceNode
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