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
Margins cannot be less than 1 pixel or so large that the text cannot be displayed.
If '''marginWidth''' is specified but [[html/attributes/marginHeight|'''marginHeight''']] is not, '''marginHeight''' is set to 0.
If the document hosted in the '''frame''' or '''iframe''' has [[css/properties/margin-left|'''margin-left''']] or [[css/properties/margin-right|'''margin-right''']] properties set either through Cascading Style Sheets (CSS) or through the [[html/attributes/leftMargin|'''leftMargin''']] or [[html/attributes/rightMargin|'''rightMargin''']] properties of the '''body''' element, then this property is ignored.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>frame</code>
*<code>iframe</code>
*<code>LayoutRect</code>
*<code>[[html/attributes/marginHeight|marginHeight]]</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}