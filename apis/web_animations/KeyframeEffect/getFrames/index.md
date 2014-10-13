{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Returns the keyframes that make up this effect as a sequence of ComputedKeyframe objects.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/web_animations/KeyframeEffect
|Example_object_name=
|Return_value_name=
|Javascript_data_type=Object
|Return_value_description=Returns a sequence of ComputedKeyFrame objects.

The value returned differs from the frames parameter passed into setFrames or the constructor for this interface in the following ways:

The normalization defined in §5.17.3 Normalizing a sequence of keyframes is applied to frames which may result in some frames being removed or re-ordered and some properties being removed. This normalization will also cause a single Keyframe object to be replaced with a sequence.
The result of computing the keyframe offset of each keyframe as defined in §4.3.1 Spacing keyframes is stored in the computedOffset member of each frame.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|Web Animations}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}