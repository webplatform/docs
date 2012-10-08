{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Initial value=manual
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=none
|Description=Indicates that all word breaking is suppressed, including at soft hyphens.
}}{{CSS Property Value
|Data Type=manual
|Description=Indicates that word breaking is allowed only where word breaking opportunities are suggested. These suggestions may come in the form of soft hyphens or hard hyphens.
}}{{CSS Property Value
|Data Type=auto
|Description=Indicates that, in addition to suggested word breaking opportunities, word breaking opportunities are allowed where determined by a hyphenation resource (dictionary). Soft hyphens take priority over other hyphenation opportunities, but are still subject to the hyphenation controlled properties.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Import_Notes====Syntax===
<code>'''-ms-hyphens: '''none '''{{!}}''' manual '''{{!}}''' auto</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203766 CSS Text Level 3], Section 5.1
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Text
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}