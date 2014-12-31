{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Sets the velocity vector of the audio source. This vector controls both the direction of travel and the speed in 3D space. This velocity relative to the listener's velocity is used to determine how much doppler shift (pitch change) to apply. The x, y, and z parameters describe a direction vector indicating direction of travel and intensity. The default value is (0,0,0).}}
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
|Method_applies_to=apis/webaudio/PannerNode
|Example_object_name=PannerNode
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
var panner = audioCtx.createPanner();
panner.setVelocity(0,0,17);
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