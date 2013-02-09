{{Page_Title}}
{{Flags
|High-level issues=Merge Candidate, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Editorial notes=Merge with [[html/elements/comment]] (and move out of html/elements, since comments are not elements.
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Comments in HTML delimit parts of the source document that are not rendered by the browser.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following is an example of an '''HTML Comment'''.
|Code=&lt;!-- This text will not appear in the browser window. --&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
Comments can contain other HTML elements. Comments do not nest.
Start and end tags are required.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 3.2.4


===Members===
The '''HTML Comment''' object has these types of members:
*[#properties Properties]


====Properties====
The '''HTML Comment''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/text|'''text''']]
|Retrieves or sets the text of the object as a string.
|}
 
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
*<code>comment</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}