{{Page_Title}}
{{Flags
|Content=Incomplete, Cleanup
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The line-height propriety specifies the height of line within the element. The minimum height within a block level elements, the calculated one for replaced inline elements. It has no effect for non-replaced inline elements like buttons or other input elements.}}
{{CSS Property
|Initial value=normal
|Applies to=all elements
|Inherited=Yes
|Media=visual
|Computed value=for <length> and <percentage> the absolute value; otherwise as specified
|Animatable=Yes
|CSS object model property=lineHeight
|CSS percentages=refer to the font size of the element itself
|Values={{CSS Property Value
|Data Type=normal
|Description=Take the height fixed by the default css of the user browser. 
In most cases, it multiplies the height of the font by 1.2.
}}{{CSS Property Value
|Data Type=<number>
|Description=The used value of the property is this number multiplied by the element's font size. Negative values are illegal.
}}{{CSS Property Value
|Data Type=<length>
|Description=The specified length is used in the calculation of the line box height: a number immediately followed by a length unit - <code>px</code>, <code>em</code>, <code>pc</code>, <code>in, <code>mm</code>. Negative values cannot be used.
}}{{CSS Property Value
|Data Type=<percentage>
|Description=The used value of the property is the percentage of the element's font size.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* setting a line-height of 1.3em to a paragraph element with a font size of 1em*/

/* with a percentage */
p { line-height: 130% }

/* with a length */
p { line-height: 1.3em}

/* with a number */
p { line-height: 1.3}
}}
}}
{{Notes_Section
|Notes====Remarks===
Line height is the distance between the descender of the font and the top of the internal leading of the font. If a formatted line contains more than one object, the maximum line height applies. In this case, negative values are not allowed.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS1 line-height
|URL=http://www.w3.org/TR/CSS1/#line-height
|Status=W3C Recommendation
|Relevant_changes=Initial definition.
}}{{Related Specification
|Name=CSS2.1 line-height
|URL=http://www.w3.org/TR/CSS2/visudet.html#propdef-line-height
|Status=W3C Recommendation
}}{{Related Specification
|Name=css3 transition
|URL=http://dev.w3.org/csswg/css3-transitions/#animatable-css
|Status=Working Draft
|Relevant_changes=Defines line-height as animatable.
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0 (1.7 or earlier)
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=7.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=1.0
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=4.6
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=1.0
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0 (1)
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=6.0
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=6.0
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=1.0
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Box Model
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}