{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=Yes
|Editorial notes=No clear examples.
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The ‘fill’ property paints the interior of the given graphical element. The area to be painted consists of any areas inside the outline of the shape. To determine the inside of the shape, all subpaths are considered, and the interior is determined according to the rules associated with the current value of the ‘fill-rule’ property. The zero-width geometric outline of a shape is included in the area to be painted.}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
|Content=The fill operation fills open subpaths by performing the fill operation as if an additional "closepath" command were added to the path to connect the last point of the subpath with the first point of the subpath. Thus, fill operations apply to both open subpaths within ‘path’ elements (i.e., subpaths without a closepath command) and ‘polyline’ elements.
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Import_Notes====Syntax===

 '''fill: '''none '''{{!}}''' currentColor '''{{!}}''' funciri '''{{!}}''' inherit

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
*[[svg/attributes/stroke|'''stroke''']]
}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}