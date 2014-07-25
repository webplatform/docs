{{Page Title}}
{{Flags|State=Not Ready|Editorial notes=summary, clean-up of MSDN import
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/HTMLTableElement
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example shows how to put text in the first cell in the first row of the first '''tBody''' object in the [[html/elements/table|'''table''']]. For each '''table''', an initial '''tBody''' object is synthesized in the HTML tree even if a '''tBody''' element does not exist in the HTML source.
|LiveURL=
|Code=
document.all.oTable.tBodies[0].rows[0].cells[0].innerText {{=}} 
   "Text for the first table cell";
}}}}
{{Notes_Section
|Notes=
===Remarks===
This collection can be indexed by name ([[html/attributes/id|'''ID''']]). If duplicate names are found, a collection of those named items is returned. Collections of duplicate names must be referenced subsequently by ordinal position.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[html/elements/table|table]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}