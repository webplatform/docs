{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Connects one AudioNode to another AudioNode.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=destination
|Data type=unsigned long
|Description=The AudioNode to connect to.
|Optional=Yes
}}{{Method Parameter
|Index=1
|Name=output
|Data type=unsigned long
|Description=An index describing which output of the AudioNode to connect from. An out-of-bound value throws an exception.
|Optional=Yes
}}{{Method Parameter
|Index=2
|Name=input
|Data type=unsigned long
|Description=An index describing which input of the destination AudioNode to connect to. An out-of-bound value throws an exception.
|Optional=Yes
}}
|Method_applies_to=apis/webaudio/AudioNode
|Example_object_name=AudioNode
|Return_value_name=
|Javascript_data_type=
|Return_value_description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var oscillator = audioCtx.createOscillator();
oscillator.connect(audioCtx.destination,1,1);
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