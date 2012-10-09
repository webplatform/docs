{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Notes_Section
|Notes=
===Remarks===
With the '''pathSegList''' property, you can  access  the base (or ''static'') contents of the [[svg/properties/d|'''d''']] attribute in a form that directly matches   the SVG syntax. If the '''d''' attribute contains an "absolute moveto (M)" and an "absolute arcto (A)" command,  '''pathSegList''' contains two entries: SVG_PATHSEG_MOVETO_ABS and SVG_PATHSEG_ARC_ABS.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204736 Scalable Vector Graphics: Paths], Section 8.5.22


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/elements/path|SVGPathElement]]</code>
*<code>[[svg/properties/animatedPathSegList|animatedPathSegList]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}
[[Category:SVG]]