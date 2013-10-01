{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Examples Needed
|Checked_Out=No
|Editorial notes='''As of time of writing, this property is not yet implemented in most browsers.'''
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|This property indicates whether the <mask-reference> is treated as a luminescence mask or as an alpha mask.}}
{{CSS Property
|Initial value=auto
|Applies to=All elements. In SVG, it applies to container elements without the <defs> element and all graphics elements.
|Inherited=No
|Media=visual
|Computed value=As specified.
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=<source-type>
|Description=May have the following values:
*'''auto''': Implicitly sets alpha or luminance, depending on the <mask-reference> value of the mask-image property. If it is of type <mask-source>, the luminance values of the mask image should be used as the mask values; if it is of type <image>, the alpha values of the mask image should be used as the mask values.
*'''alpha''': Indicates that the alpha values of the mask image should be used as the mask values. 
*'''luminance''': Indicates that the luminance values of the mask image should be used as the mask values.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* auto */
#img1 {
    mask-source-type: auto;
  }

/* alpha */
#img2 {
    mask-source-type: alpha;
  }

/* luminance */
#img3 {
    mask-source-type: luminance;
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