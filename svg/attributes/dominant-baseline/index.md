{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Topics|SVG}}
{{Notes_Section
|Notes=

===Remarks===

A ''scaled-baseline-table'' is a compound value that has three
components: a baseline identifier for the dominant baseline, a
baseline table, and a baseline table font-size.  Some values of the
property redetermine all three values; others only re-establish the
baseline table font-size.  When the default value, auto, gives an
undesired result, this property can be used to explicitly set the
desire scaled-baseline table.

|Import_Notes=

===Syntax===

 '''dominant-baseline: '''auto '''{{!}}''' use-script '''{{!}}''' no-change '''{{!}}''' reset-size '''{{!}}''' ideographic '''{{!}}''' alphabetic '''{{!}}''' hanging '''{{!}}''' mathematical '''{{!}}''' central '''{{!}}''' middle '''{{!}}''' text-after-edge '''{{!}}''' text-before-edge '''{{!}}''' inherit

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199818 Scalable Vector Graphics: Text], Section 10.9.2

}}
{{See_Also_Section
|Manual_sections=

===Related pages (MSDN)===

*[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|'''CSSStyleDeclaration''']]
*[[css/cssom/currentStyle|'''currentStyle''']]
*[[css/cssom/style|'''style''']]
*[[svg/elements/tspan|'''SVGTSpanElement''']]
*[[svg/elements/textPath|'''SVGTextPathElement''']]
*[[svg/elements/text|'''SVGTextElement''']]
*[[svg/attributes/baseline-shift|'''baselineShift''']]
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}