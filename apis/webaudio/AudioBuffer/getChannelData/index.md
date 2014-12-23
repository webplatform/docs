{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Returns the '''Float32Array''' representing the PCM audio data for the specific channel.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=channel
|Data type=unsigned long
|Description=The channel parameter is an index representing the particular channel to get data for. An index value of 0 represents the first channel. This index value MUST be less than [[apis/webaudio/AudioBuffer/numberOfChannels|'''numberOfChannels''']] or an exception will be thrown.
|Optional=No
}}
|Method_applies_to=apis/webaudio/AudioBuffer
|Example_object_name=AudioBuffer
|Return_value_name=
|Javascript_data_type=
|Return_value_description=Float32Array
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var myArrayBuffer = audioCtx.createBuffer(2, frameCount, audioCtx.sampleRate);
var nowBuffering = myArrayBuffer.getChannelData(channel);
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