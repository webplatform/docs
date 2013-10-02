{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Examples Needed
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Specifies the size of the mask images, similar to the CSS [[css/properties/background-size|background-size]] property.}}
{{CSS Property
|Initial value=auto
|Applies to=All elements. It applies to container elements without the <defs> and graphics elements in SVG.
|Inherited=No
|Media=visual
|Computed value=As specified, but with lengths made absolute.
|Animatable=No
|CSS percentages=See text.
|Values={{CSS Property Value
|Data Type=auto
|Description=The intrinsic height/width of the mask image is used.
}}{{CSS Property Value
|Data Type=contain
|Description=Scale the image, while preserving its intrinsic aspect ratio (if any), to the largest size such that both its width and height can fit inside the background positioning area.
}}{{CSS Property Value
|Data Type=cover
|Description=Scale the image, while preserving its intrinsic aspect ratio (if any), to the smallest size such that both its width and height can completely cover the background positioning area.
}}{{CSS Property Value
|Data Type=length
|Description=A floating-point number, followed by an absolute units designator (cm, mm, in, pt, or pc) or a relative units designator (em, ex, or px).
}}{{CSS Property Value
|Data Type=percentage
|Description=An integer, followed by a percent (%). A percentage value is relative to the background positioning area.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* contain */
body {
        background-color: white;
        mask-image: url(big-black-dot.jpg);
        mask-position: bottom right;
        mask-repeat: no-repeat;
        mask-size: contain;
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