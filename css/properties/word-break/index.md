{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=All elements
|Media=visual
|Inherited=Yes
|Initial value=
|Values={{CSS_Property_Value|Data Type=normal |Description=Default.
Allows line breaking within words.}}
{{CSS_Property_Value|Data Type=break-all |Description=Behaves as
'''normal'''
for CJK text, yet allows the line to break arbitrarily
for non-CJK text. This value is suited to CJK text
that contains small amounts of non-CJK text.}}
{{CSS_Property_Value|Data Type=keep-all |Description=Behaves as
'''normal'''
for non-CJK text, but disallows word breaking for
CJK text. This value is suited to
non-CJK text that includes small amounts of CJK text.}}
}}
{{Topics|CSS}}
{{Notes_Section
|Notes=
===Remarks===
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
|Import_Notes=
===Syntax===
<code>'''-ms-word-break: '''normal '''{{!}}''' break-all '''{{!}}''' keep-all</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203766 CSS Text Level 3], Section 5.2
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}223137 Unicode Standard Annex #14 -- Unicode Line Breaking Algorithm]


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
|Topic_clusters=Text
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}