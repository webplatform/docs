{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Initial value=0
|Applies to=block containers
|Inherited=Yes
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=percentage
|Description=Integer, followed by a percent sign (%) that specifies the width of the hyphenation zone, calculated with respect to the line box. 

Negative values are not allowed.
}}{{CSS Property Value
|Data Type=length
|Description=A floating-point number, followed by a relative units designator, that indicates the width of the hyphenation zone.
For more information about supported length units,
see CSS Values and Units.

Negative values are not allowed.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The '''-ms-hyphenate-limit-zone''' property enables you to control the amount of trailing whitespace permitted during hyphenation. The hyphenation zone is always at the logical right side of the padding box.
A word is considered for hyphenation only if it begins at or outside of the logical left limit of the hyphenation zone.
|Import_Notes====Syntax===
<code>'''-ms-hyphenate-limit-zone: '''''
&lt;percentage&gt;
'' '''{{!}}''' ''
&lt;length&gt;
''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203766 CSS Text Level 3], Section 5.3
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