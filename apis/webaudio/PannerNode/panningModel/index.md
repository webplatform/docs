{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Determines which spatialization algorithm will be used to position the audio in 3D space. See below for the available choices. The default is HRTF.}}
{{API_Object_Property
|Property_applies_to=apis/webaudio/PannerNode
|Read_only=No
|Example_object_name=PannerNode
|Return_value_name=
|Javascript_data_type=unsigned short
|Return_value_description=Uses one of the following constant values: 
*EQUALPOWER (0), a simple and efficient spatialization algorithm using equal-power panning; 
*HTRF (1) (default), a higher quality spatialization algorithm using a convolution with measured impulse responses from human subjects, which renders stereo output
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var audioCtx = new AudioContext();
var panner = audioCtx.createPanner();
panner.panningModel = 'HRTF';
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