{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs return type
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Creates a '''MediaStreamAudioSourceNode''' given a [[apis/webrtc/MediaStream|'''MediaStream''']]. As a consequence of calling this method, audio playback from the [[apis/webrtc/MediaStream|'''MediaStream''']] will be re-routed into the processing graph of the [[apis/webaudio/AudioContext|'''AudioContext''']].}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/webaudio/AudioContext
|Example_object_name=AudioContext
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=//it may be necessary to prefix getUserMedia and AudioContext in order to work in some browsers

//request microphone stream
navigator.getUserMedia({ audio: true }, function(stream){ 
     var context = new AudioContext();
     var micStreamSource = context.createMediaStreamSource(stream);

     micStreamSource.connect(context.destination);  //redirects mic input to speakers
}, function(){ console.log('Error getting Microphone stream'); });
}}
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