{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Add description and compatibility.
'''As of time of writing, this property is not yet implemented in most browsers.'''
|Checked_Out=Yes
|High-level issues=Needs Review
|Content=Examples Needed
}}
{{Standardization_Status|W3C Last Call Working Draft}}
{{API_Name}}
{{Summary_Section|This property is shorthand for setting [[css/properties/mask-image|mask-image]], [[css/properties/mask-mode|mask-mode]], [[css/properties/mask-repeat|mask-repeat]], [[css/properties/mask-position|mask-position]], [[css/properties/mask-clip|mask-clip]], [[css/properties/mask-origin|mask-origin]], [[css/properties/mask-composite|mask-composite]] and [[css/properties/mask-size|mask-size]]. Omitted values are set to their original properties' initial values.}}
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
<mask-layer> = <mask-reference> <masking-mode>? || <position> [ / <bg-size> ]? ||
<repeat-style> || <geometry-box> || [ <geometry-box> | no-clip ] || <compositing-operator>
</code>
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The url points to a <mask> element that is used as mask.
|Code=/* mask-reference via a url */
img {
  mask: url(#masking);
}
}}{{Single Example
|Language=CSS
|Code=/* Two mask layers (both references to mask images) that are combined with the 'add' compositing mode. */
img {
  mask: url(mask-image1.png) add, url(mask-image2.png);
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
|URL=http://dev.w3.org/fxtf/masking/
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