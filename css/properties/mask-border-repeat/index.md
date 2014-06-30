{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add description and compatibility.
'''As of time of writing, this property is not yet implemented in most browsers.'''
|Checked_Out=No
|Content=Examples Needed
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|This property specifies how the images for the sides and the middle part of the mask image are scaled and tiled. The first keyword applies to the horizontal sides, the second one applies to the vertical ones. If the second keyword is absent, it is assumed to be the same as the first, similar to the CSS [[css/properties/border-image-repeat|border-image-repeat]] property.}}
{{CSS Property
|Initial value=stretch
|Applies to=All elements. In SVG, it applies to container elements without the <defs> element and all graphics elements.
|Inherited=No
|Media=visual
|Computed value=As specified
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=stretch
|Description=The image is stretched to fill the area.
}}{{CSS Property Value
|Data Type=repeat
|Description=The image is tiled (repeated) to fill the area.
}}{{CSS Property Value
|Data Type=round
|Description=The image is tiled (repeated) to fill the area. If it does not fill the area with a whole number of tiles, the image is rescaled so that it does.
}}{{CSS Property Value
|Data Type=space
|Description=The image is tiled (repeated) to fill the area. If it does not fill the area with a whole number of tiles, the extra space is distributed around the tiles.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* explicit horizontal, explicit vertical */
#maskbox1: {
    mask-box-image-repeat: stretch repeat;
}

/* explicit horizontal, implicit vertical */
#maskbox1: {
    mask-box-image-repeat: round;
}
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Masking Level 1
|URL=https://dvcs.w3.org/hg/FXTF/raw-file/default/masking/index.html
|Status=W3C Editor's Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}