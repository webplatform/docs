{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Inserts nodes after this animation node.

If there is no parent animation group, terminate these steps.
If any of the animation nodes in nodes is an inclusive ancestor of this animation node throw a HierarchyRequestError exception and terminate these steps.
Let reference child be the next sibling of this animation node not in nodes.
Insert nodes before reference child.
}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=AnimationNode...nodes
|Data type=Object
|Description=Takes a series of AnimationNodes as a parameter
|Optional=No
}}
|Method_applies_to=apis/web_animations/AnimationNode
|Example_object_name=
|Return_value_name=
|Javascript_data_type=
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