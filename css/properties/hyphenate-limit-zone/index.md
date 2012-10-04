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
|Initial value=0
|Values={{CSS_Property_Value|Data Type=percentage |Description=Integer, followed by a percent sign (%) that specifies the width of the hyphenation zone, calculated with respect to the line box. 

Negative values are not allowed.}}
{{CSS_Property_Value|Data Type=length |Description=A floating-point number, followed by a relative units designator, that indicates the width of the hyphenation zone.
For more information about supported length units,
see CSS Values and Units.

Negative values are not allowed.}}
}}
{{Topics|CSS}}
{{Notes_Section
|Notes=
===Remarks===
The '''-ms-hyphenate-limit-zone''' property enables you to control the amount of trailing whitespace permitted during hyphenation. The hyphenation zone is always at the logical right side of the padding box.
A word is considered for hyphenation only if it begins at or outside of the logical left limit of the hyphenation zone.
|Import_Notes=
===Syntax===
<code>'''-ms-hyphenate-limit-zone: '''''
&lt;percentage&gt;
'' '''{{!}}''' ''
&lt;length&gt;
''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203766 CSS Text Level 3], Section 5.3


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