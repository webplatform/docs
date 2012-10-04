{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/document
|Read_only=
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
This property returns a value only when the user reaches the current document through a link from the previous document. Otherwise, <code>document</code>.'''referrer''' returns an empty string; it also returns an empty string when the link is from a secure site.
For example, if DocumentA.htm includes a link to DocumentB.htm, and the user clicks that link, the <code>document</code>.'''referrer''' on DocumentB.htm returns "DocumentA.htm." However, if the user is on DocumentA.htm and types DocumentB.htm into the address line or chooses the '''Open''' command from the '''File''' menu to get to DocumentB.htm, the <code>document</code>.'''referrer''' returns an empty string.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}