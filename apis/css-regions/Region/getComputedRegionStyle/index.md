{{Page_Title}}
{{Flags
|High-level issues=Stub
|Content=Incomplete, Examples Needed
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Returns styles calculated for the region, including styles from [[css/atrules/@region|'''@region''']] rules applied to ranges.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=element
|Data type=DOM Node
|Description=The element that contains the desired style settings, regardless of whether it currently appears within the region.
|Optional=No
}}{{Method Parameter
|Name=pseudoElementName
|Data type=String
|Description=The name of a CSS pseudo-element (such as "::before" or "::after") or a null value. Optional in WebKit-based browsers.
|Optional=Yes
}}
|Method_applies_to=apis/css-regions/Region
|Example_object_name=region
|Return_value_name=stylesheet
|Javascript_data_type=CSSStyleDeclaration
|Return_value_description=Returns styles calculated for the region, including styles from [[css/atrules/@region|'''@region''']] rules applied to ranges.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=Behaves the same as [[css/cssom/methods/getComputedStyle|'''getComputedStyle()''']], but incorporates CSS formatting from [[css/atrules/@region|'''@region''']] rules that may apply to individual regions.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Regions
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}