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
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example defines a two-column frame, with the first occupying 40 percent of the available width and the second occupying the remaining 60 percent.
|LiveURL=
|Code=
&lt;FRAMESET COLS{{=}}"40%, 60%"&gt;
}}
{{Single_Example
|Description=This example defines a four-column frame. The first is 50 pixels wide, and the fourth is 80 pixels wide. The second occupies two-thirds of the remaining width, while the third occupies the final third of the remaining width.
|LiveURL=
|Code=
&lt;FRAMESET COLS{{=}}"50, 2*, *, 80"&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The number of comma-separated items is equal to the number of frames contained within the '''frameSet''', while the value of each item determines the frame width.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>frameSet</code>
*<code>[[dom/properties/rows (frameSet, cols)|rows]]</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}