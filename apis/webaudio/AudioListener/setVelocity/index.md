{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Sets the velocity vector of the listener. This vector controls both the direction of travel and the speed in 3D space. This velocity relative an audio source's velocity is used to determine how much doppler shift (pitch change) to apply. The x, y, z parameters describe a direction vector indicating direction of travel and intensity. The default value is (0,0,0).}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=x
|Data type=Number
|Description=
|Optional=No
}}{{Method Parameter
|Index=1
|Name=y
|Data type=Number
|Description=
|Optional=No
}}{{Method Parameter
|Index=2
|Name=z
|Data type=Number
|Description=
|Optional=No
}}
|Method_applies_to=apis/webaudio/AudioListener
|Example_object_name=AudioListener
|Return_value_name=
|Javascript_data_type=Number
|Return_value_description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var audioCtx = new AudioContext();
var myListener = audioCtx.listener;
myListener.setVelocity(0,0,0);
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
|Status=W3C Editor's draft
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