{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Describes the relationship from the current document to the anchor specified by the [[html/attributes/href|'''href''']] attribute.}}
{{Markup_Attribute
|Applies_to=http://docs.webplatform.org/wiki/html/elements/a
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
If no values are indicated, the '''rel''' property's default relationship is an empty string. This property is used only when the [[css/cssom/properties/href|'''href''']] property is applied.
The '''Offline''', '''Search''', '''Shortcut Icon''', and '''Stylesheet''' values apply only to the '''link''' object.
The '''rel''' property is similar to the [[html/attributes/rev|'''rev''']] property, but the semantics of these two properties' link types are in the reverse direction. For example, a link from A to B with REL{{=}}"X" expresses the same relationship as a link from B to A with REV{{=}}"X". An anchor can have both '''rel''' and '''rev''' properties.
Internet Explorer 8 and later. In IE8 Standards mode, the '''rel''' content attribute locates the '''Alternate''' token regardless of its position in a space-delimited list of tokens. For example, '''rel''' will locate '''Alternate''' whether it is parsed as '''rel{{=}}"alternate stylesheet"''' or '''rel{{=}}"stylesheet alternate"'''. For more information on IE8 mode, see Defining Document Compatibility.
The '''Offline''' value is available in Microsoft Internet Explorer 5 and later. For more information about CDF files and offline favorites, see Enhancing Offline Favorites. CDF is obsolete as of Internet Explorer 7.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 12.2
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
*<code>[[html/elements/a|a]]</code>
*<code>link</code>
*<code>Reference</code>
*<code>[[html/attributes/rev|rev]]</code>
*<code>Other Resources</code>
*<code>Subscribing to Content with Web Slices</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}