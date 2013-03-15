{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Connects the [[apis/webaudio/AudioNode|'''AudioNode''']] to another [[apis/webaudio/AudioNode|'''AudioNode''']].}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=destination
|Data type=unsigned long
|Description=The [[apis/webaudio/AudioNode|'''AudioNode''']] to connect to.
|Optional=Yes
}}{{Method Parameter
|Name=output
|Data type=unsigned long
|Description=An index describing which output of the [[apis/webaudio/AudioNode|'''AudioNode''']] to connect from. An out-of-bound value throws an exception.
|Optional=Yes
}}{{Method Parameter
|Name=input
|Data type=unsigned long
|Description=An index describing which input of the destination [[apis/webaudio/AudioNode|'''AudioNode''']] to connect to. An out-of-bound value throws an exception.
|Optional=Yes
}}
|Method_applies_to=apis/webaudio/AudioNode
|Example_object_name=AudioNode
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
{{Topics|API, WebAudio}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}