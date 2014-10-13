{{Page_Title}}
{{Flags
|State=
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|See the iterationStart member of the AnimationTimingReadOnly interface.

Values less than zero are clamped to zero for the purpose of timing model calculations.

Note that the value of iterations is effectively added to the iterationStart such that an animation node with an iterationStart of ‘0.5’ and iterations of ‘2’ would still repeat twice however it would begin and end half-way through the animation node’s iteration interval.
Setting the iterationStart to a value greater than or equal to one is typically only useful in combination with an animation effect that has an iteration composite operation of ‘accumulate’.
}}
{{API_Object_Property
|Property_applies_to=apis/web animations/AnimationTimingProperties
|Read_only=No
|Example_object_name=
|Return_value_name=
|Javascript_data_type=
|Return_value_description=
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
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}