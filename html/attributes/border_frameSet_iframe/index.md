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
This property applies either to the outer '''frameSet''' element or to inner '''frameSet''' elements. When you specify the '''border''' property of the outermost '''frameSet''' element, the '''border''' properties of any inner '''frameSet''' elements are ignored. When you do not specify the '''border''' property of the outermost '''frameSet''' element, the '''border''' properties of inner '''frameSet''' elements are not ignored.
Setting a border to zero or omitting the attribute causes no border to be displayed. Supplying the border attribute without a value defaults to a single border.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>frameSet</code>
*<code>iframe</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}