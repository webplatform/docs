{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Determines which algorithm will be used to reduce the volume of an audio source as it moves away from the listener. See below for the available choices. The default is INVERSE_DISTANCE.}}
{{API_Object_Property
|Property_applies_to=apis/webaudio/PannerNode
|Read_only=No
|Example_object_name=PannerNode
|Return_value_name=
|Javascript_data_type=unsigned short
|Return_value_description=Uses one of the following constant values: 
*LINEAR_DISTANCE (0), a linear distance model which calculates distanceGain as 1 - rolloffFactor * (distance - refDistance) / (maxDistance - refDistance); 
*INVERSE_DISTANCE (1) (default), an inverse distance model which calculates distanceGain as refDistance / (refDistance + rolloffFactor * (distance - refDistance)); 
*EXPONENTIAL_DISTANCE (2), an exponential distance model which calculates distanceGain as pow(distance / refDistance, -rolloffFactor).
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var audioCtx = new AudioContext();
var panner = audioCtx.createPanner();
panner.distanceModel = 'inverse';
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