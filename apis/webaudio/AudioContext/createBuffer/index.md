{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Creates an [[apis/webaudio/AudioBuffer|AudioBuffer]] of the given size. The audio data in the buffer will be zero-initialized (silent). An exception will be thrown if the [[apis/webaudio/AudioBuffer/numberOfChannels|numberOfChannels]] or [[apis/webaudio/AudioContext/sampleRate|sampleRate]] are out-of-bounds.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=numberOfChannels
|Data type=unsigned long
|Description=Determines how many channels the buffer will have. An implementation must support at least 32 channels.
|Optional=No
}}{{Method Parameter
|Index=1
|Name=length
|Data type=unsigned long
|Description=Determines the size of the buffer in sample-frames.
|Optional=No
}}{{Method Parameter
|Index=2
|Name=sampleRate
|Data type=Number
|Description=Describes the sample-rate of the linear PCM audio data in the buffer in sample-frames per second. An implementation must support sample-rates in at least the range 22050 to 96000.
|Optional=No
}}
|Method_applies_to=apis/webaudio/AudioContext
|Example_object_name=AudioContext
|Return_value_name=
|Javascript_data_type=
|Return_value_description=AudioBuffer
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var audioCtx = new AudioContext();
var buffer = audioCtx.createBuffer(2, 22050, 44100);
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