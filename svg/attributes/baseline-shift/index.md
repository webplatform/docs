{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Needs review
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import, Needs Review
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Needed, Examples Best Practices, Needs Summary
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The ‘baseline-shift’ property allows repositioning of the dominant-baseline( a baseline-table and a baseline-table font-size which are those of the nearest block-level ancestor element and are applied to its root inline box.) relative to the dominant-baseline.}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
|Content=Name:	baseline-shift
Value:	baseline
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===

The '''baseline-shift''' property allows repositioning of the dominant
baseline relative to the dominant baseline of the parent text content
element.  The shifted object might be a subscript or superscript.
Within the shifted object, the whole baseline table is offset; not
just a single baseline.  The amount of the shift is determined by one
of the following:

*the parent text content element
*the subscript or superscript offset from the nominal font of the parent text content element
*the percent of the '''line-height''' of the parent text content element
*an absolute value.
|Import_Notes====Syntax===

 '''baseline-shift: '''baseline '''{{!}}''' sub '''{{!}}''' super '''{{!}}''' ''percentage'' '''{{!}}''' ''length''

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199818 Scalable Vector Graphics: Text], Section 10.9.2
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Scalable Vector Graphics (SVG) 1.1
|URL=http://www.w3.org/TR/SVG/text.html#BaselineShiftProperty
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSS Layout, CSS Attributes
|Manual_sections====Related pages (MSDN)===

*[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|'''CSSStyleDeclaration''']]
*[[css/cssom/currentStyle|'''currentStyle''']]
*[[css/cssom/style|'''style''']]
*[[svg/elements/tspan|'''SVGTSpanElement''']]
*[[svg/elements/textPath|'''SVGTextPathElement''']]
*[[svg/attributes/dominant-baseline|'''dominantBaseline''']]
}}
{{Topics|DOM, SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}