{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|word-break is often used when there is long generated content that is strung together without and spaces or hyphens to beak apart. A common case of this is when there is a long URL that does not have any hyphens. This case could potentially cause the breaking of the layout as it could extend past the parent element.}}
{{CSS Property
|Initial value=normal
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=specified value
|Animatable=No
|CSS percentages=Not available
|Values={{CSS Property Value
|Data Type=normal
|Description=Default.
Allows line breaking within words.
}}{{CSS Property Value
|Data Type=break-all
|Description=Behaves as
'''normal'''
for CJK text, yet allows the line to break arbitrarily
for non-CJK text. This value is suited to CJK text
that contains small amounts of non-CJK text.
}}{{CSS Property Value
|Data Type=keep-all
|Description=Behaves as
'''normal'''
for non-CJK text, but disallows word breaking for
CJK text. This value is suited to
non-CJK text that includes small amounts of CJK text.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=<div>
  <a href="#">http://example.com/this_is_a_long_href/so_we_will_use_word_break/to_keep_inside_of_div</a>
</div>
|LiveURL=http://cdpn.io/covtd
}}{{Single Example
|Language=CSS
|Code=div {
  background: #ccc;
  border: 1px solid #444;
  margin: 2em;
  padding: .5em;
  width: 300px;
  
  -ms-word-break: break-all;
  word-break: break-all;
}
|LiveURL=http://cdpn.io/covtd
}}
}}
{{Notes_Section
|Notes====Remarks===
Windows Internet Explorer 8. The '''-ms-word-break''' attribute is an extension to CSS, and can be used as a synonym for '''word-break''' in IE8 Standards mode.
When using the
'''-ms-word-break'''
attribute with a
[[html/elements/table|'''table''']],
you must set the
[[css/properties/table-layout|'''table-layout''']]
attribute to
'''fixed'''
on the
'''table'''.
The behaviors of the parameter values are detailed in
[http://go.microsoft.com/fwlink/p/?linkid{{=}}203753 CSS Text Level 3: W3C Working Draft (6 March 2007), sec. 4.1, "Line Breaking Restrictions: The 'word-break' Property"]; and in
[http://go.microsoft.com/fwlink/p/?linkid{{=}}203714 Unicode Standard Annex #14: Line Breaking Properties].
|Import_Notes====Syntax===
<code>'''-ms-word-break: '''normal '''{{!}}''' break-all '''{{!}}''' keep-all</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203766 CSS Text Level 3], Section 5.2
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}223137 Unicode Standard Annex #14 -- Unicode Line Breaking Algorithm]
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=22.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=15.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=8.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Text
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}