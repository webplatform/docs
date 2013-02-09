{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Determines which algorithm will be used to reduce the volume of an audio source as it moves away from the listener. See below for the available choices. The default is INVERSE_DISTANCE.}}
{{API_Object_Property
|Property_applies_to=apis/webaudio/PannerNode
|Read_only=No
|Example_object_name=PannerNode
|Javascript_data_type=unsigned short
|Return_value_description=Uses one of the following constant values: LINEAR_DISTANCE (0), a linear distance model which calculates distanceGain as 1 - rolloffFactor * (distance - refDistance) / (maxDistance - refDistance); INVERSE_DISTANCE (1) (default), an inverse distance model which calculates distanceGain as refDistance / (refDistance + rolloffFactor * (distance - refDistance)); EXPONENTIAL_DISTANCE (2), an exponential distance model which calculates distanceGain as pow(distance / refDistance, -rolloffFactor).
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