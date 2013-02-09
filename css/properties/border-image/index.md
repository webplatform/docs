{{Page_Title}}
{{Flags
|High-level issues=Needs Topics
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Shorthand property that defines an image to be displayed and its positioning, instead of a solid color, for 'border' property. Image can be transformed in different ways.}}
{{CSS Property
|Initial value=none
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=based on individual properties
|Animatable=No
|Values={{CSS Property Value
|Data Type=none
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=[[File:background-image.png|example base graphics file]]
<code>border-image: url("border-image.png") 30 30 repeat;</code>
[[File:bi-repeat.png|example of a repeated background-image]]

}}
}}
{{Notes_Section
|Notes=[[css/properties/border-image-slice|'''border-image-slice: fill''']] was introduced in latest recommendation and breaks backwards compatibility. If you want border-image to fill an inner area of your block you have to use this property.

===Compatibility with other properties===
[[css/properties/border-radius|'''border-radius''']] has no effect on border-image.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Backgrounds and Borders Module Level 3
|URL=http://www.w3.org/TR/css3-background/
|Status=W3C Candidate Recommendation 24 July 2012
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=10
|Firefox_supported=Yes
|Firefox_version=15
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=3.5
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Yes
|Opera_prefixed_version=10
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=4
}}
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Firefox
|Version=15+
|Note=As required by the final specification, the unprefixed version requires [[css/properties/border-style|'''border-style''']] to be different than 'none' or border-image will be ignored.
}}{{Compatibility Notes Row
|Browser=Chrome, Safari, Opera
|Version=All
|Note=Implement an early version of the spec and incorrectly display border-image when [[css/properties/border-style|'''border-style''']] is 'none'.
}}
}}
{{See_Also_Section
|Topic_clusters=Border
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}