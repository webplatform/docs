{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Asynchronously decodes the audio file data contained in the ArrayBuffer. The ArrayBuffer can, for example, be loaded from an XMLHttpRequest with the new ''responseType'' and ''response'' attributes. Audio file data can be in any of the formats supported by the audio element.

The decodeAudioData() method is preferred over the [[apis/webaudio/AudioContext/createBuffer|createBuffer()]] from ArrayBuffer method because it is asynchronous and does not block the main JavaScript thread.
}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=audioData
|Data type=String
|Description=An ArrayBuffer containing audio file data.
|Optional=No
}}{{Method Parameter
|Index=1
|Name=successCallback
|Data type=function
|Description=A callback function which will be invoked when the decoding is finished. The single argument to this callback is an [[apis/webaudio/AudioBuffer|'''AudioBuffer''']] representing the decoded PCM audio data.
|Optional=No
}}{{Method Parameter
|Index=2
|Name=errorCallback
|Data type=function
|Description=A callback function which will be invoked if there is an error decoding the audio file data.
|Optional=Yes
}}
|Method_applies_to=apis/webaudio/AudioContext
|Example_object_name=AudioContext
|Return_value_name=
|Javascript_data_type=
|Return_value_description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var audioCtx = new AudioContext();
audioCtx.decodeAudioData(audioData, function(buffer) { ... };);
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=The older callback-based system is still in the spec for legacy reasons and is currently supported across browsers that support the Web Audio API is to be superceded by the newer promise-based syntax, which is in the latest spec, but not yet supported by any browser.

See [http://webaudio.github.io/web-audio-api/ http://webaudio.github.io/web-audio-api/].
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