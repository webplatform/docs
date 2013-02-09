{{Page_Title}}
{{Flags
|Content=Examples Needed
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The text-overflow-ellipsis CSS property controls how the hint on overflowed content that is not displayed is signaled to the users. The presence of the hint is controlled with CSS property [[css/properties/text-overflow-mode|text-overflow-mode]]. Shorthand property is [[css/properties/text-overflow|text-overflow]].}}
{{CSS Property
|Initial value=U+2026
|Applies to=block-level and inline-block elements
|Inherited=No
|Media=visual
|Computed value=specified value (except for initial and inherit)
|Animatable=No
|CSS object model property=text-overflow-ellipsis
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=string | uri
|Description=The value is defined either as a string like the default UTF-8 character 'U+2026' or a URI and represents the ellipsis of text-overflow-mode property. If the value is defined as a URI it displays the image behind the URL. You can also set both values which then means they determine the overflow visual hint at the end and the hint after the element box. The latter visual hint is only displayed if there is clipped content because of the dimension limitation on the element block.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=Because the initial value (U+2026) of the overflow visual hint after the element box may not be easily rendered in some situations, the user agent may replace it by a sequence of 3 FULL STOP characters (U+002E).
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables={{Imported Compatibility Table
|Page=css/properties/text-overflow
}}
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSS Attributes, Text
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}