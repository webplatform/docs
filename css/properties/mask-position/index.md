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
|Computed value=Two keywords representing the origin and two offsets from that origin, each given as an absolute length (if given a <length>), otherwise as a percentage.
|Animatable=Yes
|CSS percentages=Refer to size of mask painting area minus size of mask image.
|Values={{CSS Property Value
|Data Type=[[css/data_types/length|length]] [[css/data_types/length|length]]
|Description=Any standard CSS units are acceptable as <code>mask-position</code> values: px, ems, rems, mm, cm etc. Note that unit values specify the distance the top left corner of the mask is away from the top left corner of the element. For more details on these units, read [[css/data_types/length|Length units]].
}}{{CSS Property Value
|Data Type=[[css/data_types/percentage|percentage]] [[css/data_types/percentage|percentage]]
|Description=Percentages are acceptable for <code>mask-position</code> values, and specify percentages of the overall width and height of the element in question. Note that percentage values specify the distance the top left corner of the mask is away from the top left corner of the element.
}}{{CSS Property Value
|Data Type=left top
|Description=<code>mask-position</code> can also be expressed as keywords: left top, top, right top, left, center, right, left bottom, bottom, right bottom. These values do not relate specifically to the position of the top left hand corner of the mask, but rather the overall position of the mask inside the element. So for example, a value of <code>right top</code> will make the right and top sides of the mask flush to the top and right sides of the element it is applied to; the top left corner ''won't'' be positioned at the top right of the element!
}}{{CSS Property Value
|Data Type=[[css/data_types/percentage|percentage]]
|Description=If only a single value is included, that is taken as the horizontal value, and the vertical value is set as <code>center</code>.
}}{{CSS Property Value
|Data Type=bottom [[css/data_types/length|length]] right [[css/data_types/length|length]]
|Description=CSS3 includes the new four value <code>mask-position</code> syntax, which allows you to choose which sides of the element you are positioning the mask relative to (values 1 and 3), and then the distance away from those sides (values 2 and 4). So this example says that you want to position the mask 10 pixels from the bottom of the element, and 15 pixels from the right. If you miss out one of the offset values, the other is assumed to be 0.
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