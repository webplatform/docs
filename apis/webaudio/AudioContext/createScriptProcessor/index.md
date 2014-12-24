{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Creates a [[apis/webaudio/ScriptProcessorNode|ScriptProcessorNode]] for direct audio processing using JavaScript. An exception will be thrown if [[apis/webaudio/ScriptProcessorNode/bufferSize|bufferSize]] or numberOfInputChannels or numberOfOutputChannels are outside the valid range.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=bufferSize
|Data type=unsigned long
|Description=Determines the buffer size in units of sample-frames. It must be one of the following values: 256, 512, 1024, 2048, 4096, 8192, 16384. This value controls how frequently the [[apis/webaudio/ScriptProcessorNode/onaudioprocess|'''onaudioprocess''']] event handler is called and how many sample-frames need to be processed each call. Lower values for [[apis/webaudio/ScriptProcessorNode/bufferSize|'''bufferSize''']] will result in a lower (better) latency. Higher values will be necessary to avoid audio breakup and glitches. The value chosen must carefully balance between latency and audio quality.
|Optional=No
}}{{Method Parameter
|Index=1
|Name=numberOfInputChannels
|Data type=unsigned long
|Description=Defaults to 2; determines the number of channels for this node's input. Values of up to 32 must be supported.
|Optional=Yes
}}{{Method Parameter
|Index=2
|Name=numberOfOutputChannels
|Data type=unsigned long
|Description=Defaults to 2; determines the number of channels for this node's output. Values of up to 32 must be supported.
|Optional=Yes
}}
|Method_applies_to=apis/webaudio/AudioContext
|Example_object_name=AudioContext
|Return_value_name=
|Javascript_data_type=
|Return_value_description=ScriptProcessorNode
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var audioCtx = new AudioContext();
myScriptProcessor = audioCtx.createScriptProcessor(1024, 1, 1);
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