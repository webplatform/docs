{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{CSS_Property
|Applies to=All elements
|Media=visual
|Inherited=Yes
|Initial value=manual
|Values={{CSS_Property_Value|Data Type=none |Description=Indicates that all word breaking is suppressed, including at soft hyphens.}}
{{CSS_Property_Value|Data Type=manual |Description=Indicates that word breaking is allowed only where word breaking opportunities are suggested. These suggestions may come in the form of soft hyphens or hard hyphens.}}
{{CSS_Property_Value|Data Type=auto |Description=Indicates that, in addition to suggested word breaking opportunities, word breaking opportunities are allowed where determined by a hyphenation resource (dictionary). Soft hyphens take priority over other hyphenation opportunities, but are still subject to the hyphenation controlled properties.}}
}}
{{Topics|CSS}}
{{Notes_Section
|Import_Notes=
===Syntax===
<code>'''-ms-hyphens: '''none '''{{!}}''' manual '''{{!}}''' auto</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203766 CSS Text Level 3], Section 5.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
|Topic_clusters=Text
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}