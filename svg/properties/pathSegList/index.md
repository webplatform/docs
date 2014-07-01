{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Unreviewed MSDN import
|Checked_Out=No
|High-level issues=Needs Flags, Stub
}}
{{Standardization_Status|}}
{{API_Name}}
{{Topics|SVG}}
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

*[[svg/elements/path|'''SVGPathElement''']]
*[[svg/properties/animatedPathSegList|'''animatedPathSegList''']]
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}
[[Category:SVG]]