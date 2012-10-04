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
This property specifies how an object is aligned with respect to its parent. For example, this allows alphabetic baselines in Roman text to stay aligned across font size changes. It defaults to the baseline with the same name as the computed value of the alignment-baseline property. That is, the position of "ideographic" alignment-point in the block-progression-direction is the position of the "ideographic" baseline in the baseline-table of the object being aligned.
One of the characteristics of international text is that there are different baselines (different alignment points) for glyphs in different scripts. For example, in horizontal writing, ideographic scripts, such as Han Ideographs, Katakana, Hiragana, and Hangul, alignment occurs with a baseline near the bottoms of the glyphs; alphabetic based scripts, such as Latin, Cyrillic, Hebrew, Arabic, align a point that is the bottom of most glyphs, but some glyphs descend below the baseline; and Indic based scripts are aligned at a point that is near the top of the glyphs.
The "EM box" is a relative measure of the height of the glyphs in the font. The "M" character fits in a box 1 EM high and 1 EM wide.
|Import_Notes=
===Syntax===
<code>'''alignment-baseline: '''auto '''{{!}}''' baseline '''{{!}}''' before-edge '''{{!}}''' text-before-edge '''{{!}}''' middle '''{{!}}''' central '''{{!}}''' after-edge '''{{!}}''' text-after-edge '''{{!}}''' ideographic '''{{!}}''' alphabetic '''{{!}}''' hanging '''{{!}}''' mathematical '''{{!}}''' inherit</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199818 Scalable Vector Graphics: Text], Section 10.9.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}