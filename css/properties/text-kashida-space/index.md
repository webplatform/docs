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
|Initial value=0%
|Values={{CSS_Property_Value|Data Type=percentage |Description=An integer, followed by a %. The value is the ratio of kashida expansion to white space expansion. 100% specifies kashida expansion only, and 0% specifies white space expansion only}}
}}
{{Topics|CSS}}
{{Notes_Section
|Notes=
===Remarks===
Windows Internet Explorer 8. The '''-ms-text-kashida-space''' attribute is an extension to CSS, and can be used as a synonym for '''text-kashida-space''' in IE8 Standards mode.
Kashida is a typographic effect that justifies lines of text by elongating characters at carefully chosen points.  It is used in Arabic writing systems.
The property can be used with any justification style where kashida style expansion is used, such as the '''auto''', '''distribute''', '''kashida''', and '''newspaper''' values of the [[css/properties/text-justify|'''-ms-text-justify''']] property.
The property is read-only for the
.
The property applies to block elements only.
|Import_Notes=
===Syntax===
<code>'''-ms-text-kashida-space: '''percentage</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203766 CSS Text Level 3], Section 8.3


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