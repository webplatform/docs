{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Asynchronously decodes the audio file data contained in the [[apis/webaudio/ArrayBuffer|'''ArrayBuffer''']]. The [[apis/webaudio/ArrayBuffer|'''ArrayBuffer''']] can, for example, be loaded from an XMLHttpRequest with the new '''responseType''' and '''response''' attributes. Audio file data can be in any of the formats supported by the audio element.

The [[apis/webaudio/AudioContext/decodeAudioData|'''decodeAudioData()''']] method is preferred over the [[apis/webaudio/AudioContext/createBuffer|'''createBuffer()''']] from [[apis/webaudio/ArrayBuffer|'''ArrayBuffer''']] method because it is asynchronous and does not block the main JavaScript thread.
}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=audioData
|Data type=String
|Description=An [[apis/webaudio/ArrayBuffer|'''ArrayBuffer''']] containing audio file data.
|Optional=No
}}{{Method Parameter
|Name=successCallback
|Data type=function
|Description=A callback function which will be invoked when the decoding is finished. The single argument to this callback is an [[apis/webaudio/AudioBuffer|'''AudioBuffer''']] representing the decoded PCM audio data.
|Optional=No
}}{{Method Parameter
|Name=errorCallback
|Data type=function
|Description=A callback function which will be invoked if there is an error decoding the audio file data.
|Optional=Yes
}}
|Method_applies_to=apis/webaudio/AudioContext
|Example_object_name=AudioContext
}}
{{Examples_Section
|Not_required=Yes
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