{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs spec reference, example
|Checked_Out=No
|High-level issues=Stub
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Just like [[dom/Document/getElementsByClassName|Document/getElementsByClassName]] except that it only works within the scope of this ShadowRoot's shadow tree.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=classNames
|Data type=String
|Description=A space separated list of classes.
|Optional=No
}}
|Method_applies_to=dom/shadowdom/ShadowRoot
|Javascript_data_type=Object
|Return_value_description=A live [[dom/HTMLCollection|HTMLCollection]] of elements with the given class names.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=Use of this method is discouraged. See [[dom/HTMLCollection|HTMLCollection]]. However, that article has not been vetted for vendor bias, it is an unreviewed import, and the performance implications described may be browser (IE) specific.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM, Shadow DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}