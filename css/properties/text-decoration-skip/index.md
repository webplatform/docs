{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|This property will specify what parts of content that must be skipped over that has text-decoration specified.}}
{{CSS Property
|Initial value=objects
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS percentages=Not available
|Values={{CSS Property Value
|Data Type=none
|Description=Will not skip anything and the text-decoration will be drawn for all text content
}}{{CSS Property Value
|Data Type=images
|Description=Will skip an object such as image if it is an inline replacement
}}{{CSS Property Value
|Data Type=spaces
|Description=Will skip white space that can include:
* regular spaces - U+0020
* tabs - U+0009
* nbsp - U+00A0
* ideographic space - U+3000
* all fixed width spaces - examples: U+2000 to U+200A, U+202F and U+205F
* any adjacent letter-spacing or word-spacing
}}{{CSS Property Value
|Data Type=ink
|Description=Will skip over where any glyphs are drawn. Such is the case where it will interrupt the decoration line so that the text can show through where otherwise the text decoration would cross over. 

Note: The UA also may skip over small distances on the right or the left side of the glyph outline
}}{{CSS Property Value
|Data Type=box-decoration
|Description=Will skip over the box's margin, border, and padding areas.

**Note: It is not known yet if this is a needed value**
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=This property inherits so the descendent elements can have different setting.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Text Decoration Module Level 3
|URL=http://www.w3.org/TR/css-text-decor-3/
|Status=Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Text
|External_links=* https://developer.mozilla.org/en-US/docs/Web/CSS/CSS3
* http://www.w3.org/TR/css-text-decor-3/
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/gg721763(v=expression.40).aspx
|HTML5Rocks_link=
}}