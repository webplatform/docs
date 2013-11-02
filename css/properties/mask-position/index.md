{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Examples Needed
|Checked_Out=No
|Editorial notes='''As of time of writing, this property is not yet implemented in most browsers.'''
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|This property sets the initial position of a mask image. Position can be specified in terms of percentages of the distance from upper left corner (original point) or using the keywords '''top, left, center, right''', or '''bottom''', similar to the CSS [[css/properties/background-position|background-position]] property.}}
{{CSS Property
|Initial value=center
|Applies to=All elements. In SVG, it applies to container elements without the <defs> element and all graphics elements.
|Inherited=No
|Media=visual
|Computed value=A list, each item consisting of two keywords representing the origin and two offsets from that origin, each given as an absolute length (if given a <length>), otherwise as a percentage.
|Animatable=Yes
|CSS percentages=Refer to size of mask painting area minus size of mask image.
|Values={{CSS Property Value
|Data Type=<percentage>
|Description=The first number represents the percentage of distance away from the left side of the page, the second number represents the percentage of distance away from the upper side of the page. With an initial value pair of 0% 0%, the mask image is placed at the upper left corner of the page. With a value pair of 30% 70%, the mask image is be placed at the point 30% across and 70% down the page.
}}{{CSS Property Value
|Data Type=<length>
|Description=The first number represents the distance away from the left side of the page, the second number represents the distance away from the upper side of the page.
}}{{CSS Property Value
|Data Type=top
|Description=Equivalent to 0% for second (vertical) number.
}}{{CSS Property Value
|Data Type=bottom
|Description=Equivalent to 100% for second (vertical) number.
}}{{CSS Property Value
|Data Type=left
|Description=Equivalent to 0% for first (horizontal) number.
}}{{CSS Property Value
|Data Type=right
|Description=Equivalent to 100% for first (horizontal) number.
}}{{CSS Property Value
|Data Type=center
|Description=Equivalent to 50% 50%.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* bottom right */
body {
	background-color: white;
	mask-image: url(big-black-dot.jpg);
        mask-position: bottom right;
	mask-repeat: no-repeat;
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