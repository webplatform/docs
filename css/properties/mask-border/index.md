{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Examples Needed
|Checked_Out=No
|Editorial notes='''As of time of writing, this property is not yet implemented in most browsers.'''
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|This property is shorthand for setting [[css/properties/mask-box-image-source|mask-box-image-source]], [[css/properties/mask-box-image-slice|mask-box-image-slice]], [[css/properties/mask-box-image-width|mask-box-image-width]], [[css/properties/mask-box-image-outset|mask-box-image-outset]], and [[css/properties/mask-box-image-repeat|mask-box-image-repeat]]. Omitted values are set to their original properties' initial values.}}
{{CSS Property
|Initial value=See individual properties.
|Applies to=See individual properties.
|Inherited=No
|Media=visual
|Computed value=See individual properties.
|Animatable=No
|CSS percentages=See individual properties.
|Values={{CSS Property Value
|Data Type=<mask-box-image-source>
|Description=See [css/properties/mask-box-image-source|mask-box-image-source]].
}}{{CSS Property Value
|Data Type=<mask-box-image-slice>
|Description=See [css/properties/mask-box-image-slice|mask-box-image-slice]].
}}{{CSS Property Value
|Data Type=<mask-box-image-width>
|Description=See [css/properties/mask-box-image-width|mask-box-image-width]].
}}{{CSS Property Value
|Data Type=<mask-box-image-outset>
|Description=See [css/properties/mask-box-image-outset|mask-box-image-outset]].
}}{{CSS Property Value
|Data Type=<mask-box-image-repeat>
|Description=See [css/properties/mask-box-image-repeat|mask-box-image-repeat]].
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* mask-box-source (-slice) / -width / (-outset) -repeat */
#maskbox1 {
    mask-box-image: url(#someMask) / 5% / stretch;
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