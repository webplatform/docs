{{Page_Title|text-emphasis-style}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>text-emphasis-style</code> property applies special emphasis marks to an element's text.}}
{{CSS Property
|Initial value=none
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=‘none’, a pair of keywords representing the shape and fill, or a string
|Animatable=No
|CSS object model property=textEmphasisStyle
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=none
|Description=No emphasis marks.
}}{{CSS Property Value
|Data Type=filled
|Description=The shape is filled with solid color.
}}{{CSS Property Value
|Data Type=open
|Description=The shape is hollow.
}}{{CSS Property Value
|Data Type=dot
|Description=Display small circles as marks. The filled dot is U+2022 ‘•’, and the open dot is U+25E6 ‘◦’.
}}{{CSS Property Value
|Data Type=circle
|Description=Display large circles as marks. The filled circle is U+25CF ‘●’, and the open circle is U+25CB ‘○’.
}}{{CSS Property Value
|Data Type=double-circle
|Description=Display double circles as marks. The filled double-circle is U+25C9 ‘◉’, and the open double-circle is U+25CE ‘◎’.
}}{{CSS Property Value
|Data Type=triangle
|Description=Display triangles as marks. The filled triangle is U+25B2 ‘▲’, and the open triangle is U+25B3 ‘△’.
}}{{CSS Property Value
|Data Type=sesame
|Description=Display sesames as marks. The filled sesame is U+FE45 ‘﹅’, and the open sesame is U+FE46 ‘﹆’.
}}{{CSS Property Value
|Data Type=<string>
|Description=Display the given string as marks. Authors should not specify more than one character in <string>. The UA may truncate or ignore strings consisting of more than one grapheme cluster.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=
|Code=p {
  /*text-emphasis-style: shape;*/
  text-emphasis-style: dot;		
}
|LiveURL=http://code.webplatform.org/gist/6133332
}}{{Single Example
|Language=CSS
|Description=
|Code=p {
  /*text-emphasis-style: <string>;*/
  text-emphasis-style: "^";		
}
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Text Decoration Module Level 3
|URL=http://www.w3.org/TR/css-text-decor-3/
|Status=W3C Candidate Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_prefixed_supported=Yes
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=Yes
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}