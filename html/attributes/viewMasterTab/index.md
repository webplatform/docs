{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Deletion Candidate
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
Tabbing order goes from every tab stop within the viewlink to every tab stop in the primary document, based on sequence and [[html/attributes/tabIndex|'''tabIndex''']] value. By default, the master element participates in the tab sequence of the primary document, even if there are no tab stops defined within the viewlink.
When using a viewlink, the '''body''' element inside the viewlink is not tabbable by default; the author must set the [[html/attributes/tabIndex|'''tabIndex''']] property if the behavior is designed to display a focus rectangle on the linked document. Setting the '''tabIndex''' property on the '''body''' of the document fragment causes the [[dom/events/focus|'''onfocus''']] and [[dom/events/activate|'''onactivate''']] events to fire when the viewlink document '''body''' receives focus.
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
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>Reference</code>
*<code>[[dom/properties/viewLink|viewLink]]</code>
*<code>Conceptual</code>
*<code>Introduction to Viewlink</code>
*<code>About Element Behaviors</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}