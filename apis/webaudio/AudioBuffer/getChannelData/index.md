{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Returns the '''Float32Array''' representing the PCM audio data for the specific channel.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=channel
|Data type=unsigned long
|Description=The channel parameter is an index representing the particular channel to get data for. An index value of 0 represents the first channel. This index value MUST be less than [[apis/webaudio/AudioBuffer/numberOfChannels|'''numberOfChannels''']] or an exception will be thrown.
|Optional=No
}}
|Method_applies_to=apis/webaudio/AudioBuffer
|Example_object_name=AudioBuffer
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