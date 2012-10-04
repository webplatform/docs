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
This property is applied only to text written in a horizontal [[css/properties/writing-mode|'''writingMode''']].
The glyph orientation affects the amount that the current text position advances as each glyph is rendered. When the inline-progression-direction is vertical and the '''glyphOrientationVertical''' property results in an orientation angle that is a multiple of 180 degrees, the current text position is incremented according to the vertical metrics of the glyph. Otherwise, if the '''glyphOrientationVertical''' property results in an orientation angle that is not a multiple of 180 degrees, the current text position is incremented according to the horizontal metrics of the glyph.
|Import_Notes=
===Syntax===
<code>'''glyph-orientation-vertical: '''auto '''{{!}}''' ''
&lt;angle&gt;
'' '''{{!}}''' inherit</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199818 Scalable Vector Graphics: Text], Section 10.7.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[svg/elements/tspan|SVGTSpanElement]]</code>
*<code>[[svg/elements/textPath|SVGTextPathElement]]</code>
*<code>[[svg/elements/text|SVGTextElement]]</code>
*<code>[[svg/attributes/glyph-orientation-horizontal|glyphOrientationHorizontal]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}