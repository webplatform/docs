{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=apis/web_animations/Animation
|Read_only=No
|Example_object_name=myAnimation
|Return_value_name=myEffect
|Javascript_data_type=
|Return_value_description=The effect parameter, an ECMAScript value passed to the Animation constructor or to the animate operation of the Animatable interface, may specify an EffectCallback, an AnimationEffect, a Keyframe a sequence of Keyframes, or null. However, since callback functions and dictionaries are not distinguishable in WebIDL, we define the processing of this parameter for ECMAScript here in prose.

The procedure for converting an effect to an IDL value with parameter effect is as follows:

If effect is null,
Return null.
If effect is a platform object that implements AnimationEffect,
return the IDL value that is a reference to the that platform object.
If IsCallable(effect) is true,
Return the result of applying the procedure for converting an ECMAScript value to an IDL callback function type to effect using EffectCallback as the callback function type.
Otherwise,
Return a new KeyframeEffect object constructed passing effect as the frames parameter.
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