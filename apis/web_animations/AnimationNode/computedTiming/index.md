{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Returns the calculated timing properties for this animation node. This is comparable to the computed style of an Element, window.getComputedStyle(elem).

Although several of the attributes of the this object are common to the AnimationTiming object returned by the timing attribute, they have the following differences:

duration – returns the calculated value of the iteration duration. If timing.duration is the string auto or any unsupported value, this attribute will return the current calculated value of the intrinsic iteration duration.
fill – the auto value is replaced with the specific FillMode depending on the type of animation node (see §5.8.1 The FillMode enumeration).
easing – unrecognised or unsupported values are replaced with the string linear.
}}
{{API_Object_Property
|Property_applies_to=apis/web_animations/AnimationNode
|Read_only=Yes
|Example_object_name=
|Return_value_name=
|Javascript_data_type=Object
|Return_value_description=returns a ComputedTimingProperties object.
|Example_value_name=
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