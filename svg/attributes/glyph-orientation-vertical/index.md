{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Needs all content
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===

This property is applied only to text written in a horizontal [[css/properties/writing-mode|'''writingMode''']].

The glyph orientation affects the amount that the current text position advances as each glyph is rendered.  When the inline-progression-direction is vertical and the '''glyphOrientationVertical''' property results in an orientation angle that is a multiple of 180 degrees, the current text position is incremented according to the vertical metrics of the glyph.  Otherwise, if the '''glyphOrientationVertical''' property results in an orientation angle that is not a multiple of 180 degrees, the current text position is incremented according to the horizontal metrics of the glyph.
|Import_Notes====Syntax===

 '''glyph-orientation-vertical: '''auto '''{{!}}''' ''angle'' '''{{!}}''' inherit

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199818 Scalable Vector Graphics: Text], Section 10.7.2
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
*[[svg/attributes/glyph-orientation-horizontal|'''glyphOrientationHorizontal''']]
}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}