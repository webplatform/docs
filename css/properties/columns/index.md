{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|This property describes the width of columns in multicolumn elements.}}
{{CSS Property
|Initial value=Auto
|Applies to=Non-replaced block-level elements (except table elements), table cells, and inline-block elements
|Inherited=No
|Media=visual
|Computed value=The absolute length, zero or larger
|Animatable=No
|Values={{CSS Property Value
|Data Type=column-width
|Description=Describes the <length> of the optimal column width. The actual column width may be wider (to fill the available space), or narrower (only if the available space is smaller than the specified column width). Specified values must be greater than 0. Column count will be determined at *auto*.
}}{{CSS Property Value
|Data Type=column-count
|Description=Describes the ideal column count as a strictly positive <integer> where the content of the element will be flowed. The column width will be set at *auto*.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Makes 3 columns at auto width
|Code=#columns {
  -moz-columns: auto 3;  /* Firefox */
  -webkit-columns: auto 3;  /* Safari and Chrome */
  columns: auto 3;
}
|LiveURL=http://code.webplatform.org/gist/6288803
}}
}}
{{Notes_Section
|Import_Notes====Formal syntax===
<code>'''columns: '''''column-width'' '''{{!}}{{!}}''' ''column-count''</code>
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=21
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=14
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=5.1
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Multi-Column
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}