{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Schedules a sound to playback at an exact time, with options.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=when
|Data type=Number
|Description=Describes at what time (in seconds) the sound should start playing. It is in the same time coordinate system as [[apis/webaudio/AudioContext/currentTime|'''AudioContext.currentTime''']]. If 0 is passed in for this value or if the value is less than '''currentTime''', then the sound will start playing immediately. start may only be called one time and must be called before stop is called or an exception will be thrown.
|Optional=No
}}{{Method Parameter
|Index=1
|Name=offset
|Data type=Number
|Description=Describes the offset time in the buffer (in seconds) where playback will begin. This parameter is optional with a default value of 0 (playing back from the beginning of the buffer).
|Optional=Yes
}}{{Method Parameter
|Index=2
|Name=duration
|Data type=Number
|Description=Describes the duration of the portion (in seconds) to be played. This parameter is optional, with the default value equal to the total duration of the [[apis/webaudio/AudioBuffer|'''AudioBuffer''']] minus the offset parameter. Thus if neither offset nor duration are specified then the implied duration is the total duration of the [[apis/webaudio/AudioBuffer|'''AudioBuffer''']].
|Optional=Yes
}}
|Method_applies_to=apis/webaudio/AudioBufferSourceNode
|Example_object_name=AudioBufferSourceNode
|Return_value_name=
|Javascript_data_type=
|Return_value_description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Play the entire sound from the beginning.
|Code=source.start();
|LiveURL=
}}{{Single Example
|Language=JavaScript
|Description=Play, after a 1 second delay, starting at second 3, the next 10 seconds of the sound (seconds 3 through 12).
|Code=source.start(1,3,10);
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
|Name=Web Audio API
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