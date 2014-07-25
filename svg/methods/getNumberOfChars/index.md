{{Page Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
|State=Not Ready
|Editorial notes=No editing form
}}
{{Standardization_Status|}}
{{API_Name}}
{{Topics|SVG}}
{{Notes_Section
|Notes=

===Remarks===

The total number of characters  includes referenced characters from '''tref''' reference, regardless of whether they  are  rendered.

The total number of characters  is  effectively equivalent to the length of the [[dom/properties/textContent|'''textContent''']] attribute from the [http://go.microsoft.com/fwlink/p/?linkid{{=}}203747 DOM Level 3 Core] specification (section 1.4), if that attribute also expands '''tref'''  elements.
|Import_Notes=

===Syntax===

  retVal = ''object.''getNumberOfChars();

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199818 Scalable Vector Graphics: Text], Section 10.17.1

}}
{{See_Also_Section
|Manual_sections=

===Related pages (MSDN)===

*[[svg/elements/text|'''SVGTextElement''']]
*[[svg/elements/textPositioning|'''SVGTextPositioningElement''']]
*[[svg/elements/tspan|'''SVGTSpanElement''']]
*[[svg/elements/textPath|'''SVGTextPathElement''']]
*[[svg/elements/etextContent|'''ISVGTextContentElement''']]
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}

[[Category:SVG]]