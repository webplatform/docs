{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Notes_Section
|Notes=
===Remarks===
The total text advance distance includes the advance value on the glyphs (horizontal or vertical), kerning effects, letter-spacing effects, word-spacing effects, and adjustments because of the  [[svg/properties/dx|'''dx''']] and [[svg/properties/dy|'''dy''']] attributes on [[svg/elements/tspan|'''tSpan''']] elements.
If multiple consecutive characters are rendered inseparably (for example, as a single glyph or a sequence of glyphs, or because the range encompasses half of a surrogate pair), and  if the ''nchars'' parameter is greater than 0, the measured range (i.e., total advance distance) is expanded so that each of the inseparable characters are included.
|Import_Notes=
===Syntax===
<div class{{=}}"code">float retVal {{=}} ''object.''getSubStringLength(charnum, nchars);</div>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199818 Scalable Vector Graphics: Text], Section 10.17.1


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