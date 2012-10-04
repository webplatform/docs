{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Notes_Section
|Notes=
===Remarks===
The total number of characters  includes referenced characters from <code>tref</code> reference, regardless of whether they  are  rendered.
The total number of characters  is  effectively equivalent to the length of the [[dom/properties/textContent|'''textContent''']] attribute from the [http://go.microsoft.com/fwlink/p/?linkid{{=}}203747 DOM Level 3 Core] specification (section 1.4), if that attribute also expands <code>tref</code>  elements.
|Import_Notes=
===Syntax===
<div class{{=}}"code"> retVal {{=}} ''object.''getNumberOfChars();</div>
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
*<code>[[svg/elements/etextContent|ISVGTextContentElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}