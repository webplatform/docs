{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
|Content=Incomplete
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|An [[apis/webaudio/AudioDestinationNode|AudioDestinationNode]] with a single input representing the final destination for all audio (to be rendered to the audio hardware, i.e., speakers). All [[apis/webaudio/AudioNode|AudioNode]]s actively rendering audio will directly or indirectly connect to the destination node.}}
{{API_Object_Property
|Property_applies_to=apis/webaudio/AudioContext
|Read_only=Yes
|Example_object_name=AudioContext
|Return_value_name=
|Javascript_data_type=
|Return_value_description=AudioDestinationNode
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var audioCtx = new AudioContext();
gainNode.connect(audioCtx.destination);
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