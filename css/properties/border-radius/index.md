{{Page_Title}}
{{Flags
|Content=Examples Needed
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Initial value=0
|Applies to=all elements, except the 'table' element when border-collapse is collapse
|Inherited=Yes
|Media=visual
|Computed value=as specified by individual properties
|Animatable=Yes
|Values={{CSS Property Value
|Description=Denotes the size of the circle radius or the semi-major and semi-minor axes of the ellipsis. It can be expressed in any unit allowed by the CSS <length> data types. Negative values are invalid.
}}{{CSS Property Value
|Description=Denotes the size of the circle radius, or the semi-major and semi-minor axes of the ellipsis, using percentage values. Percentages for the horizontal axe refer to the width of the box, percentages for the vertical axe refer to the height of the box. Negative values are invalid.
}}
|Syntax=The syntax of the first radius allows one to four values:
* border-radius: radius
* border-radius: top-left-and-bottom-right top-right-and-bottom-left
* border-radius: top-left top-right-and-bottom-left bottom-right
* border-radius: top-left top-right bottom-right bottom-left 

The syntax of the second radius also allows one to four values
* border-radius: (first radius values) / radius
* border-radius: (first radius values) / top-left-and-bottom-right top-right-and-bottom-left
* border-radius: (first radius values) / top-left top-right-and-bottom-left bottom-right
* border-radius: (first radius values) / top-left top-right bottom-right bottom-left

border-radius: inherit
|Value_Name=percentage
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=5.0
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=4.0
|Firefox_supported=Yes
|Firefox_version=4.0
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=3.0
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.5
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.0
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=3.1
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.2
|Android_prefixed_supported=Yes
|Android_prefixed_version=2.1
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=15.0
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_phone_supported=Unknown
|IE_phone_version=
|IE_phone_prefixed_supported=Unknown
|IE_phone_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=11.0
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=4.0
|Safari_mobile_prefixed_supported=Yes
|Safari_mobile_prefixed_version=3.2
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
== Example ==

<syntaxhighlight lang="css" line start="0" highlight="2">
border: solid 10px;
border-radius: 40px 10px;
</syntaxhighlight>


{{Major_Style_Issue|main_message=This article does not include a complete compatibility table.}}