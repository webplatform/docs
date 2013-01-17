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

The glyph orientation affects the amount that the current text position advances as each glyph is rendered.  When the reference orientation direction is horizontal and the '''glyphOrientationHorizontal''' results in an orientation angle that is a multiple of 180 degrees, the current text position is incremented according to the horizontal metrics of the glyph.  Otherwise, if the '''glyphOrientationHorizontal''' results in an orientation angle that is not a multiple of 180 degrees,  the current text position is incremented according to the vertical metrics of the glyph.
|Import_Notes=

===Syntax===

 '''glyph-orientation-horizontal: ''' ''angle'' '''{{!}}''' inherit

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199818 Scalable Vector Graphics: Text], Section 10.7.2

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
*[[svg/attributes/glyph-orientation-vertical|'''glyphOrientationVertical''']]
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}