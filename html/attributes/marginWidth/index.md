{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets or retrieves the left and right margin widths before displaying the text in a frame.}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
Margins cannot be less than 1 pixel or so large that the text cannot be displayed.
If '''marginWidth''' is specified but [[html/attributes/marginHeight|'''marginHeight''']] is not, '''marginHeight''' is set to 0.
If the document hosted in the '''frame''' or '''iframe''' has [[css/properties/margin-left|'''margin-left''']] or [[css/properties/margin-right|'''margin-right''']] properties set either through Cascading Style Sheets (CSS) or through the [[html/attributes/leftMargin|'''leftMargin''']] or [[html/attributes/rightMargin|'''rightMargin''']] properties of the '''body''' element, then this property is ignored.
|Import_Notes====Syntax===
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>frame</code>
*<code>iframe</code>
*<code>LayoutRect</code>
*<code>[[html/attributes/marginHeight|marginHeight]]</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}