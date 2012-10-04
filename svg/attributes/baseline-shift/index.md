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
The '''baseline-shift''' property allows repositioning of the dominant baseline relative to the dominant baseline of the parent text content element. The shifted object might be a subscript or superscript. Within the shifted object, the whole baseline table is offset; not just a single baseline. The amount of the shift is determined by one of the following:
*the parent text content element
*the subscript or superscript offset from the nominal font of the parent text content element
*the percent of the <code>line-height</code> of the parent text content element
*an absolute value.

|Import_Notes=
===Syntax===
<code>'''baseline-shift: '''baseline '''{{!}}''' sub '''{{!}}''' super '''{{!}}''' ''
&lt;percentage&gt;
'' '''{{!}}''' ''
&lt;length&gt;
''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199818 Scalable Vector Graphics: Text], Section 10.9.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[svg/elements/tspan|SVGTSpanElement]]</code>
*<code>[[svg/elements/textPath|SVGTextPathElement]]</code>
*<code>[[svg/attributes/dominant-baseline|dominantBaseline]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}