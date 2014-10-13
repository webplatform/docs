{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|The spacing mode to use for this animation effect.}}
{{API_Object_Property
|Property_applies_to=apis/web_animations/KeyframeEffect
|Read_only=No
|Example_object_name=
|Return_value_name=
|Javascript_data_type=Object
|Return_value_description=Returns a DOMString object.

Recognized values are defined by the following grammar:

distribute | paced({ident}) | paced
{ident} here is an identifier as defined by CSS3 Values [CSS3VAL].

The meaning of each value is as follows:

distribute
Use the distribute keyframe spacing mode.
paced({ident})
Use the paced keyframe spacing mode with the property name indicated by {ident} as the paced property.

For example, paced(transform) would indicate that the keyframes should be spaced such that changes to the transform property occur at a constant rate.
paced
Use the paced keyframe spacing mode.

The paced property to use is the first property specified in the first keyframe in the list of keyframes associated with this animation effect when sorting the CSS property names in ascending order by Unicode codepoint.

As a result, changes to the keyframes may cause the paced property to change.

Note: this behavior is generally not useful for keyframes specifying more than one property. It is provided for consistency with MotionPathEffect and as a convenience for keyframe animation effects that specify only one property.
All other values are treated as "distribute" for the purpose of animation model calculations.
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