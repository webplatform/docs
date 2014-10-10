{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Creates a deep copy of this AnimationGroup object using the following procedure.

Let source be this AnimationGroup object, the object to be cloned.
Let cloned timing be a new AnimationTimingProperties object whose members are assigned the value of the attribute with the same name on source.timing.
Let cloned children be an empty sequence of AnimationNode objects.
For each child in source.children, append the result of calling child.clone() to cloned children.
Return a new AnimationGroup object created by calling the AnimationGroup constructor with parameters AnimationGroup(cloned children, cloned timing).

}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/web_animations/AnimationGroup
|Example_object_name=
|Return_value_name=
|Javascript_data_type=Object
|Return_value_description=
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