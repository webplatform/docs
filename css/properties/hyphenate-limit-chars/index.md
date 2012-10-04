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
|Initial value=auto
|Values={{CSS_Property_Value|Data Type=auto |Description=Corresponds to a value of <code>5 2 2</code>, indicating a 5-character word limit, 2 characters required before a hyphenation break, and 2 characters required following a hyphenation break.}}
{{CSS_Property_Value|Data Type=integer |Description=One to three integer values, corresponding to the word limit, the minimum number of characters required before a hyphenation break, and the minimum number of characters required following a hyphenation break, respectively.



If the third value is missing it is equal to the second.

If the second and third values are missing they are given a value of '''auto'''.

Negative values are not allowed.}}
}}
{{Topics|CSS}}
{{Notes_Section
|Import_Notes=
===Syntax===
<code>'''-ms-hyphenate-limit-chars: '''auto '''{{!}}''' ''
&lt;integer&gt;
'' {1,3}</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203766 CSS Text Level 3], Section 5.4


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