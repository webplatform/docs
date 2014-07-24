{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add description and compatibility.
'''As of time of writing, this property is not yet implemented in most browsers.'''
|Checked_Out=No
|High-level issues=Needs Review
|Content=Examples Needed
}}
{{Standardization_Status|W3C Last Call Working Draft}}
{{API_Name}}
{{Summary_Section|This property sets the width of the mask box image, similar to the CSS [[css/properties/border-image-width|border-image-width]] property.}}
{{CSS Property
|Initial value=auto
|Applies to=All elements. In SVG, it applies to container elements without the <defs> element and all graphics elements.
|Inherited=No
|Media=visual
|Computed value=All <length>s made absolute, otherwise as specified.
|Animatable=No
|CSS percentages=Relative to width/height of the mask box image area.
|Values={{CSS Property Value
|Data Type=auto
|Description=If specified, the mask box image width is the intrinsic width or height (whichever is applicable) of the corresponding image slice (see [[css/properties/mask-border-slice|mask-border-slice]]). If the image does not have the required intrinsic dimension then the corresponding ''border-width'' is used.
}}{{CSS Property Value
|Data Type=length
|Description=Represents pixels if the image is a raster image or vector coordinates if the image is a vector image.
}}{{CSS Property Value
|Data Type=percentage
|Description=Refers to the size of the mask border image area: the width of the area for horizontal offsets, the height for vertical offsets.
}}{{CSS Property Value
|Data Type=number
|Description=Represents multiples of the corresponding computed ''border-width''.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* auto */
#maskbox1: {
    mask-border-width: auto;
}

/* percentage */
#maskbox2: {
    mask-border-width: 5%;
}
}}{{Single Example
|Language=CSS
|Code=.exampleone {
    -webkit-mask-border: url('mask.png');
}

.exampletwo {
    -webkit-mask-border: url('logo.png') 100 100 0 0 round round;
}
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Masking Level 1
|URL=http://www.w3.org/TR/css-masking-1/
|Status=W3C Last Call Working Draft
}}{{Related Specification
|Name=CSS Masking Level 1
|URL=http://dev.w3.org/fxtf/css-masking-1/
|Status=W3C Editor’s Draft
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