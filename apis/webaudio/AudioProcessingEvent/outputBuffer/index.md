{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|An [[apis/webaudio/AudioBuffer|'''AudioBuffer''']] where the output audio data should be written. It will have a number of channels equal to the '''numberOfOutputChannels''' parameter of the [[apis/webaudio/AudioContext/createScriptProcessor|'''createScriptProcessor()''']] method. Script code within the scope of the [[apis/webaudio/ScriptProcessorNode/onaudioprocess|'''onaudioprocess''']] function is expected to modify the '''Float32Array''' arrays representing channel data in this [[apis/webaudio/AudioBuffer|'''AudioBuffer''']]. Any script modifications to this [[apis/webaudio/AudioBuffer|'''AudioBuffer''']] outside of this scope will not produce any audible effects.}}
{{API_Object_Property
|Property_applies_to=apis/webaudio/AudioProcessingEvent
|Read_only=Yes
|Example_object_name=AudioProcessingEvent
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