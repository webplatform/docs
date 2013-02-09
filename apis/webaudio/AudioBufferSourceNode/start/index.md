{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Schedules a sound to playback at an exact time.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=when
|Data type=Number
|Description=Describes at what time (in seconds) the sound should start playing. It is in the same time coordinate system as [[apis/webaudio/AudioContext/currentTime|'''AudioContext.currentTime''']]. If 0 is passed in for this value or if the value is less than '''currentTime''', then the sound will start playing immediately. start may only be called one time and must be called before stop is called or an exception will be thrown.
|Optional=No
}}{{Method Parameter
|Name=offset
|Data type=Number
|Description=Describes the offset time in the buffer (in seconds) where playback will begin. This parameter is optional with a default value of 0 (playing back from the beginning of the buffer).
|Optional=Yes
}}{{Method Parameter
|Name=duration
|Data type=Number
|Description=Describes the duration of the portion (in seconds) to be played. This parameter is optional, with the default value equal to the total duration of the [[apis/webaudio/AudioBuffer|'''AudioBuffer''']] minus the offset parameter. Thus if neither offset nor duration are specified then the implied duration is the total duration of the [[apis/webaudio/AudioBuffer|'''AudioBuffer''']].
|Optional=Yes
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
{{Topics|Audio}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}