{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|clone
Creates a copy of this Animation object using the following procedure.

Let source be the Animation object to clone, that is, this object.
Let cloned timing be a new AnimationTimingInput object whose members are assigned the value of the attribute with the same name on source.timing.
The AnimationEffect is cloned depending on the type of source.effect as follows,
If source.effect is an Animation object,
Let cloned effect be the result of calling source.effect.clone().
If source.effect is an EffectCallback object,
Let cloned effect be source.effect.
Otherwise,
Let cloned effect be null.
Return a new Animation object created by calling the Animation constructor with parameters Animation(source.target, cloned effect, cloned timing).
}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/web animations/Animation
|Example_object_name=myAnimation
|Return_value_name=myMimic
|Javascript_data_type=
|Return_value_description=Return a new Animation object created by calling the Animation constructor with parameters Animation(source.target, cloned effect, cloned timing).
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