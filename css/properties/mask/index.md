{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Examples Needed
|Checked_Out=Yes
|Editorial notes='''As of time of writing, this property is not yet implemented in most browsers.'''
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Shorthand property for other ''mask-'' properties.}}
{{CSS Property
|Initial value=See individual properties.
|Applies to=All elements. In SVG, it applies to container elements without the <defs> element and all graphics elements.
|Inherited=No
|Media=visual
|Computed value=See individual properties.
|Animatable=No
|CSS percentages=See individual properties.
|Values={{CSS Property Value
|Data Type=<mask-layer>
|Description=Where
<code>
<mask-layer> = <mask-reference> <source-type>?
              || <position> [ / <bg-size> ]? || <repeat-style>
              || <box> || [ <box> | no-clip ]
</code>
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* mask-reference via a url */
img {
  mask: url(#masking);
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