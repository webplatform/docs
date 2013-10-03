{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Examples Needed
|Checked_Out=No
|Editorial notes='''As of time of writing, this property is not yet implemented in most browsers.'''
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|This property specifies inward offsets from the top, right, bottom, and left edges of the mask image, dividing it into nine regions: four corners, four edges, and a middle. The middle image part is discarded and treated as fully transparent black unless the ''fill'' keyword is present. The four values set the top, right, bottom and left offsets in that order, similar to the CSS [[css/properties/border-image-slice|border-image-slice]] property.}}
{{CSS Property
|Initial value=0 fill
|Applies to=All elements. In SVG, it applies to container elements without the <defs> element and all graphics elements.
|Inherited=No
|Media=visual
|Computed value=As specified.
|Animatable=No
|CSS percentages=Refer to the size of the mask image.
|Values={{CSS Property Value
|Data Type=<percentage>
|Description=Refers to the size of the mask box image area: the width of the area for horizontal offsets, the height for vertical offsets.
}}{{CSS Property Value
|Data Type=<number>
|Description=Represents pixels if the image is a raster image or vector coordinates if the image is a vector image.
}}{{CSS Property Value
|Data Type=fill
|Description=If present, causes the middle part of the mask image to be preserved. If omitted, the middle part of the mask image is discarded, i.e., treated as empty.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* numbers, fill */
#maskbox1: {
    mask-box-image-slice: 30 50 30 50 fill;
}

/* percentages, no fill */
#maskbox2: {
    mask-box-image-slice: 25% 10% 20% 25%;
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