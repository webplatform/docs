{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=All elements
|Media=visual
|Inherited=Yes
|Initial value=normal
|Values={{CSS_Property_Value|Data Type=normal |Description=Default. No change in glyph substitution or positioning occurs.}}
{{CSS_Property_Value|Data Type=feature-tag-value |Description=Comma-separated list of one or more OpenType layout feature tags (each with an optional toggle). See Remarks for examples of correct syntax, plus a table of the most common feature tags and their definitions.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
The version of this property using a vendor prefix, '''-ms-font-feature-settings''', has been deprecated. To ensure compatibility in the future, applications using this property with a vendor prefix should be updated accordingly.
The [http://go.microsoft.com/fwlink/p/?LinkID{{=}}150692 OpenType specification] defines many advanced typographic features that can be implemented by font designers. For instance, you can define vertical positioning for a font, substitute glyph forms with ligatures, contextual alternates, stylistic alternates, or swashes, include a set of small caps, and more.
Each defined feature has a corresponding feature tag that identifies its function and effects. Font developers can also define their own features. A feature's tag determines what the feature does and whether to implement it. The following table lists some of the most common feature tags and their definitions.
For the full list of OpenType layout features, see [http://go.microsoft.com/fwlink/p/?LinkId{{=}}236359 OpenType layout feature tag registry].
{| class="wikitable"
|-
!Tag
!Description
|-
|'''kern'''
|Kerning
|-
|'''smcp'''
|Small capitals
|-
|'''liga'''
|Standard ligatures
|-
|'''dlig'''
|Discretionary ligatures
|-
|'''ss01''', '''ss02''', '''ss03''' ... '''ss20'''
|Stylistic sets (font-specific)
|-
|'''swsh'''
|Swash
|-
|'''tnum'''
|Tabular figures
|-
|'''lnum'''
|Lining figures
|-
|'''onum'''
|Oldstyle figures
|}
 
If you are unfamiliar with the font features listed in this table, the CSS Fonts Module Level 3 specification has good explanations and visual examples of each feature in Section 6, "[http://go.microsoft.com/fwlink/?LinkID{{=}}236360 Font feature properties]." Be aware that, though the properties listed correspond to OpenType layout features that might be supported, the properties themselves ('''font-kerning''', '''font-variant-*''', and so on) are not supported.
|Import_Notes=
===Syntax===
<code>'''font-feature-settings: '''normal '''{{!}}''' ''feature-tag-value'' [, ''feature-tag-value'' ]*</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197161 CSS 3 Fonts], Section 6.12


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
|Topic_clusters=Fonts
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}