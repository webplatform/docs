{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Describes which direction the listener is pointing in the 3D cartesian coordinate space. Both a front vector and an up vector are provided. In simple human terms, the front vector represents which direction the person's nose is pointing. The up vector represents the direction the top of a person's head is pointing. These values are expected to be linearly independent (at right angles to each other). The x, y, z parameters represent a front direction vector in 3D space, with the default value being (0,0,-1). The xUp, yUp, zUp parameters represent an up direction vector in 3D space, with the default value being (0,1,0).}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=x
|Data type=Number
|Optional=No
}}{{Method Parameter
|Name=y
|Data type=Number
|Optional=No
}}{{Method Parameter
|Name=z
|Data type=Number
|Optional=No
}}{{Method Parameter
|Name=xUp
|Data type=Number
|Optional=No
}}{{Method Parameter
|Name=yUp
|Data type=Number
|Optional=No
}}{{Method Parameter
|Name=zUp
|Data type=Number
|Optional=No
}}
|Method_applies_to=apis/webaudio/AudioListener
|Example_object_name=AudioListener
|Javascript_data_type=Number
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
{{Topics|Audio}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}