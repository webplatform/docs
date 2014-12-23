{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|The speed at which to render the audio stream. The default [[apis/webaudio/AudioBufferSourceNode/playbackRate|playbackRate]] value is 1. This parameter is a-rate.}}
{{API_Object_Property
|Property_applies_to=apis/webaudio/AudioBufferSourceNode
|Read_only=No
|Example_object_name=AudioBufferSourceNode
|Return_value_name=
|Javascript_data_type=
|Return_value_description=AudioParam
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var source = audioCtx.createBufferSource();
// play 25% faster than normal speed (1.0)
source.playbackRate.value = 1.25; 

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