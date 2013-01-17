{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following ellipse, centered within a  400 by 400 pixel square, has a major axis of 400 pixels (that is, 2 &middot; '''rx''') and a minor axis of 300 pixels (that is, 2 &middot; [[svg/properties/ry (SVGEllipseElement)|'''ry''']]).
|LiveURL=
|Code=
<syntaxhighlight lang="xml">
<?xml version="1.0" standalone="no"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">
<svg width="400px" height="400px"
     viewBox="0 0 400 400" version="1.1" xmlns="http://www.w3.org/2000/svg">
  <desc>Major and Minor Axes of an SVG Ellipse</desc>
  <rect width="100%" height="100%" style="stroke: red; fill: none;"/>
  <ellipse cx="200" cy="200" rx="200" ry="150" style="fill: none; stroke: black;"/>
</svg>
</syntaxhighlight>
}}}}
{{Topics|SVG}}
{{Notes_Section
|Import_Notes=

===Syntax===

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204737 Scalable Vector Graphics: Basic Shapes], Section 9.8.3

}}
{{See_Also_Section
|Manual_sections=

===Related pages (MSDN)===

*[[svg/elements/ellipse|'''SVGEllipseElement''']]
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}
[[Category:SVG]]