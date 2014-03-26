{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/Selection
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
Windows Internet Explorer 9 does not currently support multiple or disjointed selections in standards mode. This property always returns a 1 with a valid selection. It returns a 0 if [[dom/Selection/removeRange|'''removeRange''']] or [[dom/Selection/removeAllRanges|'''removeAllRanges''']] have been applied, though calling [[dom/Selection/isCollapsed|'''isCollapsed''']] is recommended instead to detect an empty range.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 7.6.1
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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}