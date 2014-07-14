{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Review
|Content=Examples Needed
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|This property helps determine an inline box's block-progression dimension, derived from the text-height and font-size properties for non-replaced elements, the height or the width for replaced elements, and the stacked block-progression dimension for inline-block elements. The block-progression dimension determines the position of the padding, border and margin for the element.}}
{{CSS Property
|Initial value=auto
|Applies to=Inline elements and parents of elements with display:ruby-text.
|Inherited=Yes
|Media=visual
|Computed value=As specified, except for initial and inherit
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=auto
|Description=The block-progression dimension is based either on the em square determined by the computed element font-size property value, or the cell-height (ascender + descender) related to the computed element font-size as chosen by the user agent.
}}{{CSS Property Value
|Data Type=font-size
|Description=The block-progression dimension is based on the em square as determined by the computed element font-size.
}}{{CSS Property Value
|Data Type=text-size
|Description=The block-progression dimension is based on the cell-height (ascender + descender) related to the computed element font-size.
}}{{CSS Property Value
|Data Type=max-size
|Description=The block-progression dimension is based on the maximum extents toward the before-edge and after-edge of the box (obtained by considering all child elements located on the same line), ruby annotations (elements with "display:ruby-text"), and baseline shifted elements.
}}{{CSS Property Value
|Data Type=<number>
|Description=The block progression dimension is based on ''number'' times the em square as determined by the computed font-size.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* auto */
.inlinebox { text-height: auto; }

/* font-size */
.inlinebox { text-height: font-size; }

/* number */
.inlinebox { text-height: 3; }
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Line Layout Module
|URL=http://dev.w3.org/csswg/css-inline/
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