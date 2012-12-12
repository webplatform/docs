{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets or retrieves the number of columns in the table.}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example defines a two-column frame, with the first occupying 40 percent of the available width and the second occupying the remaining 60 percent.
|Code=&lt;FRAMESET COLS{{=}}"40%, 60%"&gt;
}}{{Single Example
|Description=This example defines a four-column frame. The first is 50 pixels wide, and the fourth is 80 pixels wide. The second occupies two-thirds of the remaining width, while the third occupies the final third of the remaining width.
|Code=&lt;FRAMESET COLS{{=}}"50, 2*, *, 80"&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The number of comma-separated items is equal to the number of frames contained within the '''frameSet''', while the value of each item determines the frame width.
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
*<code>frameSet</code>
*<code>[[dom/properties/rows (frameSet, cols)|rows]]</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}