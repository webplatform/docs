{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{CSS_Property
|Applies to=block containers
|Media=visual
|Inherited=Yes
|Initial value=no-limit
|Values={{CSS_Property_Value|Data Type=no-limit |Description=Indicates that hyphenation is not limited based on the number of consecutive hyphenated lines. In the flow above the consecutive hyphenated lines limit would be an infinitely large positive number.}}
{{CSS_Property_Value|Data Type=integer |Description=Indicates the maximum number of successive hyphenated lines.

For instance, if <code>2</code>, then no more than 2 successive lines may end with a hyphenated word. If <code>0</code> then no lines may end with a hyphenated word. (Hyphenation is effectively disabled.)

Negative values are not allowed.}}
}}
{{Topics|CSS}}
{{Notes_Section
|Import_Notes=
===Syntax===
<code>'''-ms-hyphenate-limit-lines: '''no-limit '''{{!}}''' ''
&lt;integer&gt;
''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203766 CSS Text Level 3], Section 5.5


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