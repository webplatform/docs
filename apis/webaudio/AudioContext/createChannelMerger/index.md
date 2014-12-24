{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Creates a [[apis/webaudio/ChannelMergerNode|ChannelMergerNode]] representing a channel merger. An exception will be thrown for invalid parameter values.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=numberOfOutputs
|Data type=Number
|Description=Determines the number of outputs. Values of up to 32 must be supported. If not specified, then 6 will be used.
|Optional=No
}}
|Method_applies_to=apis/webaudio/AudioContext
|Example_object_name=AudioContext
|Return_value_name=
|Javascript_data_type=
|Return_value_description=ChannelMergerNode
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var audioCtx = new AudioContext();
var merger = audioCtx.createChannelMerger(2);
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