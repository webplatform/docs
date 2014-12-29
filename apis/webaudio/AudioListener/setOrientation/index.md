{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Describes which direction the listener is pointing in the 3D cartesian coordinate space. Both a front vector and an up vector are provided. In human terms, the front vector represents which direction the person's nose is pointing. The up vector represents the direction the top of a person's head is pointing. These values are expected to be linearly independent (at right angles to each other). The x, y, z parameters represent a front direction vector in 3D space, with the default value being (0,0,-1). The xUp, yUp, zUp parameters represent an up direction vector in 3D space, with the default value being (0,1,0).}}
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
}}{{Method Parameter
|Index=3
|Name=xUp
|Data type=Number
|Description=
|Optional=No
}}{{Method Parameter
|Index=4
|Name=yUp
|Data type=Number
|Description=
|Optional=No
}}{{Method Parameter
|Index=5
|Name=zUp
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
myListener.setOrientation(0,0,-1,0,1,0);
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