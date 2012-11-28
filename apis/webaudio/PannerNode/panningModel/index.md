{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Determines which spatialization algorithm will be used to position the audio in 3D space. See below for the available choices. The default is HRTF.}}
{{API_Object_Property
|Property_applies_to=apis/webaudio/PannerNode
|Read_only=No
|Example_object_name=PannerNode
|Javascript_data_type=unsigned short
|Return_value_description=Uses one of the following constant values: EQUALPOWER (0), a simple and efficient spatialization algorithm using equal-power panning; HTRF (1), a higher quality spatialization algorithm using a convolution with measured impulse responses from human subjects, which renders stereo output; SOUNDFIELD (2), an algorithm which spatializes multi-channel audio using sound field algorithms.
}}
{{Examples_Section
|Not_required=Yes
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