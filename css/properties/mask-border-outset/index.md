{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add description and compatibility.
'''As of time of writing, this property is not yet implemented in most browsers.'''
|Checked_Out=No
|High-level issues=Needs Review
|Content=Examples Needed
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|This property specifies the amount by which the mask box image area extends beyond the border box, similar to the CSS [[css/properties/border-image-outset|border-image-outset]] property. The four values set the outsets on the top, right, bottom, and left sides in that order.}}
{{CSS Property
|Initial value=0
|Applies to=All elements. In SVG, it applies to container elements without the <defs> element and all graphics elements.
|Inherited=No
|Media=visual
|Computed value=All <length>s made absolute, otherwise as specified.
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=length
|Description=Represents pixels if the image is a raster image or vector coordinates if the image is a vector image.
}}{{CSS Property Value
|Data Type=number
|Description=Represents multiples of the corresponding computed ''border-width''.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* length */
#maskbox1: {
    mask-box-image-outset: 30 50 30 50;
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