{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Examples Needed
|Checked_Out=No
|Editorial notes='''As of time of writing, this property is not yet implemented in most browsers.'''
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|For elements rendered as a single box, specifies the mask positioning area. For elements rendered as multiple boxes (e.g., inline boxes on several lines, boxes on several pages) specifies which boxes ''box-decoration-break'' operates on to determine the mask positioning area(s).}}
{{CSS Property
|Initial value=padding-box
|Applies to=All elements. In SVG, it applies to container elements without the element and all graphics elements.
|Inherited=No
|Media=visual
|Computed value=As specified.
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=padding-box
|Description=The position is relative to the padding box. (For single boxes, ''0 0'' is the upper left corner of the padding edge; ''100% 100%'' is the lower right corner.)
}}{{CSS Property Value
|Data Type=border-box
|Description=The position is relative to the border box (painting box for objects without associated layout box).
}}{{CSS Property Value
|Data Type=content-box
|Description=The position is relative to the content box (object bounding box for objects without associated layout box).
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* padding-box */
body {
	background-color: white;
	mask-image: url(big-black-dot.jpg);
        mask-position: bottom right;
	mask-repeat: no-repeat;
        mask-origin: padding-box;
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