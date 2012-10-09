{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
'''filterUnits''' defines the coordinate system for the filter attributes. If <code>filterUnits{{=}}"userSpaceOnUse"</code>, all attributes represent values in the current user coordinate system that is in place at the time when the filter is referenced.

If <code>filterUnits{{=}}"objectBoundingBox"</code>, then all attributes represent fractions or percentages of the bounding box on the referencing element.

If attribute <code>filterUnits</code> is not specified, then the effect is the same as  specifying a value of <code>objectBoundingBox</code>.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}226062 Scalable Vector Graphics: Filter Effects], Section 15.25.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/elements/filter|SVGFilterElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}
[[Category:SVG]]