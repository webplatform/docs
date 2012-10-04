{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Topics|HTML}}
{{Notes_Section
|Notes=
===Remarks===
Care should be taken when the '''noWrap''' property is used in conjunction with the [[html/attributes/width  (img, input elements)|'''width''']] attribute of [[html/elements/table|'''table''']] or '''td''' elements.
Wordwrap still occurs in a '''td''' element that has its [[html/attributes/width  (img, input elements)|'''WIDTH''']] attribute set to a value smaller than the unwrapped content of the cell, even if the '''noWrap''' property is set to true. Therefore, the '''WIDTH''' attribute takes precedence over the '''noWrap''' property in this scenario.
If a '''td''' element has its '''noWrap''' set to true and the [[html/attributes/width  (img, input elements)|'''WIDTH''']] attribute of its [[html/elements/table|'''table''']] element is set to a smaller dimension than the rendered content of the '''td''' element, wordwrap does not occur. In this case, the '''noWrap''' setting takes precedence over the '''WIDTH''' attribute.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 11.2.6 (Deprecated)


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>body</code>
*<code>dd</code>
*<code>div</code>
*<code>dt</code>
*<code>td</code>
*<code>th</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}