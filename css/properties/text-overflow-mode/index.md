{{Page_Title}}
{{Flags
|Content=Examples Needed
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The text-overflow-mode CSS property controls the presence and position of the hint on overflowed content that is not displayed is signaled to the users. The constitution of the hint is controlled with CSS property [[css/properties/text-overflow-ellipsis|text-overflow-ellipsis]]. Shorthand property is [[css/properties/text-overflow|text-overflow]].}}
{{CSS Property
|Initial value=clip
|Applies to=block-level and inline-block elements
|Inherited=No
|Media=visual
|Computed value=specified value (except for initial and inherit)
|Animatable=No
|CSS object model property=text-overflow-mode
|Values={{CSS Property Value
|Data Type=clip
|Description=Default. Simply clips the content and does not display ellipsis for text-overflow.
}}{{CSS Property Value
|Data Type=ellipsis
|Description=Display ellipsis (...) for text overflow after the last letter that entirely fits into a line.
}}{{CSS Property Value
|Data Type=ellipsis-word
|Description=Display ellipsis (...) for text overflow after the last word that entirely fits into a line.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=This property only applies to text overflow in the inline direction (horizontal, in normal Western text). Inline overflow occurs when the text in a line overflows the available width without a breaking opportunity. To force overflow to occur and ellipses to be applied, the author must apply the nowrap value to the white-space property on the element, or wrap the content in a <NOBR> tag. If there is no breaking opportunity (for example, the width is narrow or there is a long word that does not break well), then overflow may occur without nowrap being applied. This property on the element must be set to something other than visible, the default, in order for ellipsis to be rendered. The best choice is to set overflow to hidden. Setting overflow to scroll or auto will also work, but will show scrollbars. The hidden text can be selected by selecting the ellipses. When selected, the ellipses will disappear and be replaced by the text to the extent of the layout area. This property offers an efficient alternative to building ellipses in Dynamic HTML (DHTML). As ellipses may be rendered many times on a single page, using this property can significantly speed up performance.
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
|Manual_sections=http://docs.webplatform.org/wiki/css/properties/text-overflow
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}