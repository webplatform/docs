{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=All elements
|Media=visual
|Inherited=No
|Initial value=
|Values={{CSS_Property_Value|Data Type=none |Description=Default. No effect takes place—that is, no extra space is added.}}
{{CSS_Property_Value|Data Type=ideograph-alpha |Description=Creates extra spacing between runs of ideographic and non-ideographic text, such as Latin-based, Cyrillic, Greek, Arabic, or Hebrew text.}}
{{CSS_Property_Value|Data Type=ideograph-numeric |Description=Creates extra spacing between runs of ideographic text and numeric characters.}}
{{CSS_Property_Value|Data Type=ideograph-parenthesis |Description=Creates extra spacing between a normal (non-wide) parenthesis and an ideograph.}}
{{CSS_Property_Value|Data Type=ideograph-space |Description=Extends the width of the space character when it is adjacent to ideographs.}}
}}
{{Topics|CSS}}
{{Notes_Section
|Notes=
===Remarks===
Windows Internet Explorer 8. The '''-ms-text-autospace''' attribute is an extension to CSS, and can be used as a synonym for '''text-autospace''' in IE8 Standards mode.
An ideograph is a character in an Asian writing system that represents a concept or an idea, but not a particular word or pronunciation.
|Import_Notes=
===Syntax===
<code>'''-ms-text-autospace: '''none '''{{!}}''' ideograph-alpha '''{{!}}''' ideograph-numeric '''{{!}}''' ideograph-parenthesis '''{{!}}''' ideograph-space</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203766 CSS Text Level 3], Section 9.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/cssom/styleSheet|styleSheet]]</code>
|Topic_clusters=Text
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}