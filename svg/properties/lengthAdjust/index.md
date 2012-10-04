{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Notes_Section
|Notes=
===Remarks===
Indicates the type of adjustments to perform in order to make the rendered length of the text match the value specified on the [[svg/properties/textLength|'''textLength''']] attribute.
A value of <code>spacing</code> indicates that only the advance values are adjusted. The glyphs themselves are not stretched or compressed.
A value of <code>spacingAndGlyphs</code> indicates that the advance values are adjusted and the glyphs themselves are stretched or compressed in one axis (that is, in a direction parallel to the inline-progression direction).
The correct start and end positions for the text strings are guaranteed, but the locations of intermediate glyphs are not predictable because browsers might employ advanced algorithms to stretch or compress text strings in order to balance correct start and end positioning with optimal typography.
Be aware that, for a text string that contains ''n'' characters, the adjustments to the advance values often occur only for ''n''-1 characters, whereas stretching or compressing of the glyphs will be applied to all ''n'' characters.
If the attribute is not specified, the effect is as if a value of <code>spacing</code> were specified.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199818 Scalable Vector Graphics: Text], Section 10.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/elements/text|SVGTextElement]]</code>
*<code>[[svg/elements/textPositioning|SVGTextPositioningElement]]</code>
*<code>[[svg/elements/tspan|SVGTSpanElement]]</code>
*<code>[[svg/elements/textPath|SVGTextPathElement]]</code>
*<code>[[svg/elements/etextContent|SVGTextContentElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}