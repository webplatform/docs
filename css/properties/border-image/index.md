{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Undescriptive Title
|Content=Examples Needed
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|This property displays an image instead of a solid color for 'border' property. Image can be transformed in different ways.}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=none
}}{{CSS Property Value
|Data Type=border-image-source
}}{{CSS Property Value
|Data Type=border-image-slice
}}{{CSS Property Value
|Data Type=border-image-width
}}{{CSS Property Value
|Data Type=border-image-outset
}}{{CSS Property Value
|Data Type=border-image-repeat
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=border-image: url('image.png') fill auto repeat;
}}
}}
{{Notes_Section
|Notes=Firefox 15 requires [[css/properties/border-style|'''border-style''']] to be set (for example 'solid') in order to display.
Also, [[css/properties/border-image-slice|'''border-image-slice: fill''']] was introduced in latest recommendation and breaks backwards compatibility. If you want border-image to fill an inner area of your block you have to use this property.
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
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Firefox_supported=Yes
|Firefox_version=15
|Firefox_prefixed_supported=Yes
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Yes
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Yes
}}
|Mobile_rows=
|Notes_rows=
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