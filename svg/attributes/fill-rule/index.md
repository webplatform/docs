{{Page_Title}}
{{Flags
|High-level issues=Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The ‘fill-rule’ property indicates the algorithm which is to be used to determine what parts of the canvas are included inside the shape. For a simple, non-intersecting path, it is intuitively clear what region lies "inside"; however, for a more complex path, such as a path that intersects itself or where one subpath encloses another, the interpretation of "inside" is not so obvious.}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
|Content=The ‘fill-rule’ property provides two options for how the inside of a shape is determined:

nonzero
This rule determines the "insideness" of a point on the canvas by drawing a ray from that point to infinity in any direction and then examining the places where a segment of the shape crosses the ray. Starting with a count of zero, add one each time a path segment crosses the ray from left to right and subtract one each time a path segment crosses the ray from right to left. After counting the crossings, if the result is zero then the point is outside the path. Otherwise, it is inside.

evenodd
This rule determines the "insideness" of a point on the canvas by drawing a ray from that point to infinity in any direction and counting the number of path segments from the given shape that the ray crosses. If this number is odd, the point is inside; if even, the point is outside.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following drawing illustrates the nonzero rule:
|Code=View this example as SVG (SVG-enabled browsers only)
|LiveURL=http://www.w3.org/TR/SVG/images/painting/fillrule-nonzero.svg
}}{{Single Example
|Language=CSS
|Description=The following drawing illustrates the evenodd rule:
|Code=View this example as SVG (SVG-enabled browsers only)
|LiveURL=http://www.w3.org/TR/SVG/images/painting/fillrule-evenodd.svg
}}
}}
{{Notes_Section
|Usage=(Note: the above explanations do not specify what to do if a path segment coincides with or is tangent to the ray. Since any ray will do, one may simply choose a different ray that does not have such problem intersections.)
|Import_Notes====Syntax===

 '''fill-rule: '''nonzero '''{{!}}''' evenodd '''{{!}}''' inherit

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199816 Scalable Vector Graphics: Painting, Filling, Stroking and Marker Symbols], Section 11.3
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

*[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|'''CSSStyleDeclaration''']]
*[[css/cssom/currentStyle|'''currentStyle''']]
*[[css/cssom/style|'''style''']]
*[[svg/elements/tspan|'''SVGTSpanElement''']]
*[[svg/elements/textPath|'''SVGTextPathElement''']]
*[[svg/elements/text|'''SVGTextElement''']]
*[[svg/elements/path|'''SVGPathElement''']]
*[[svg/elements/rect|'''SVGRectElement''']]
*[[svg/elements/circle|'''SVGCircleElement''']]
*[[svg/elements/ellipse|'''SVGEllipseElement''']]
*[[svg/elements/line|'''SVGLineElement''']]
*[[svg/elements/polyline|'''SVGPolylineElement''']]
*[[svg/elements/polygon|'''SVGPolygonElement''']]
}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}