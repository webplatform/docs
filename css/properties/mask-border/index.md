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
{{Summary_Section|This property is shorthand for setting [[css/properties/mask-border-source|mask-border-source]], [[css/properties/mask-border-slice|mask-border-slice]], [[css/properties/mask-border-width|mask-border-width]], [[css/properties/mask-border-outset|mask-border-outset]], and [[css/properties/mask-border-repeat|mask-border-repeat]]. Omitted values are set to their original properties' initial values.}}
{{CSS Property
|Initial value=See individual properties.
|Applies to=See individual properties.
|Inherited=No
|Media=visual
|Computed value=See individual properties.
|Animatable=No
|CSS percentages=See individual properties.
|Values={{CSS Property Value
|Data Type=<mask-border-source>
|Description=See [[css/properties/mask-border-source|mask-border-source]].
}}{{CSS Property Value
|Data Type=<mask-border-slice>
|Description=See [[css/properties/mask-border-slice|mask-border-slice]].
}}{{CSS Property Value
|Data Type=<mask-border-width>
|Description=See [[css/properties/mask-border-width|mask-border-width]].
}}{{CSS Property Value
|Data Type=<mask-border-outset>
|Description=See [[css/properties/mask-border-outset|mask-border-outset]].
}}{{CSS Property Value
|Data Type=<mask-border-repeat>
|Description=See [[css/properties/mask-border-repeat|mask-border-repeat]].
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* mask-border-source (-slice) / -width / (-outset) -repeat */
#maskbox1 {
    mask-border: url(#someMask) / 5% / stretch;
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