{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Creates a MediaStreamAudioSourceNode, given a [[apis/webrtc/MediaStream|MediaStream]]. As a consequence of calling this method, audio playback from the [[apis/webrtc/MediaStream|MediaStream]] will be re-routed into the processing graph of the [[apis/webaudio/AudioContext|AudioContext]].}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/webaudio/AudioContext
|Example_object_name=AudioContext
|Return_value_name=
|Javascript_data_type=
|Return_value_description=MediaStreamAudioSourceNode
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=//it may be necessary to prefix getUserMedia and AudioContext in order to work in some browsers

//request microphone stream
navigator.getUserMedia({ audio: true }, function(stream){ 
     var context = new AudioContext();
     var micStreamSource = context.createMediaStreamSource(stream);

     micStreamSource.connect(context.destination);  //redirects mic input to speakers
}, function(){ console.log('Error getting Microphone stream'); });
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