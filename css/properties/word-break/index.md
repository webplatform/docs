{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The word-break property is often used when there is long generated content that is strung together without and spaces or hyphens to beak apart. A common case of this is when there is a long URL that does not have any hyphens. This case could potentially cause the breaking of the layout as it could extend past the parent element.}}
{{CSS Property
|Initial value=normal
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=specified value
|Animatable=No
|CSS object model property=wordBreak
|CSS percentages=Not available
|Values={{CSS Property Value
|Data Type=normal
|Description=Default property. Words break according to their usual rules.
}}{{CSS Property Value
|Data Type=break-all
|Description=In addition to <tt>normal</tt> soft wrap opportunities, lines may break between any two letters (except where forbidden by the [[css/properties/line-break|'''line-break''']] property). Hyphenation is not applied. This option is used mostly in a context where the text is predominantly using CJK (Chinese/Japanese/Korean) characters with few non-CJK excerpts and it is desired that the text be better distributed on each line.
}}{{CSS Property Value
|Data Type=keep-all
|Description=Implicit soft wrap opportunities between letters are suppressed, i.e. breaks are prohibited between pairs of letters (except where opportunities exist due to dictionary-based breaking). Otherwise this option is equivalent to <tt>normal</tt>. In this style, sequences of CJK characters do not break.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A simple example showing multiple <code>&lt;div&gt;</code>s, identical in style except that they have different <code>word-break</code> properties applied to them.
|Code=&lt;p&gt;This example using break-all will stay within the box border.&lt;/p&gt;
&lt;div class="break-all"&gt;
  http://www.exampleurl.com/this-is-a-long-url/it-will-not-break-at-hypens
&lt;/div&gt;

&lt;p&gt;This example using keep-all will break where there are hyphens.&lt;/p&gt;
&lt;div class="keep-all"&gt;
  http://www.exampleurl.com/this-is-a-long-url/it-will-break-at-hypens
&lt;/div&gt;
|LiveURL=http://code.webplatform.org/gist/6392109
}}{{Single Example
|Language=CSS
|Code=div {
  background: yellow;
  border: 1px solid #444;
  margin: 1em;
  padding: .5em;
  width: 200px;
  font-family: sans-serif;
}

.break-all {
  -ms-word-break: break-all; 
  word-break: break-all;
}

.keep-all {
  -ms-word-break: keep-all;
  word-break: keep-all;
}
|LiveURL=http://code.webplatform.org/gist/6392109
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
<code>'''word-break: '''normal '''{{!}}''' break-all '''{{!}}''' keep-all</code>
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