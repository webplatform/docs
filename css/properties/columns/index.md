{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|This property is a shorthand property for setting column-width or column-count. Omitted values are set to their initial value of <tt>auto</tt>.}}
{{CSS Property
|Initial value=Auto
|Applies to=Non-replaced block-level elements (except table elements), table cells, and inline-block elements
|Inherited=No
|Media=visual
|Computed value=The absolute length, zero or larger
|Animatable=No
|Values={{CSS Property Value
|Data Type=column-width
|Description=Any of the values available to [[css/properties/column-width|'''column-width''']] property. The default value is <tt>auto</tt>.
}}{{CSS Property Value
|Data Type=column-count
|Description=Any of the values available to [[css/properties/column-count|'''column-count''']] property. The default value is <tt>auto</tt>.
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}