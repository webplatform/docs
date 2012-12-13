{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Gets or sets one or more values that specify glyph substitution and positioning in fonts that include OpenType layout features.}}
{{CSS Property
|Initial value=normal
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=normal
|Description=Default. No change in glyph substitution or positioning occurs.
}}{{CSS Property Value
|Data Type=feature-tag-value
|Description=Comma-separated list of one or more OpenType layout feature tags (each with an optional toggle). See Remarks for examples of correct syntax, plus a table of the most common feature tags and their definitions.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
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
|Import_Notes====Syntax===
<code>'''font-feature-settings: '''normal '''{{!}}''' ''feature-tag-value'' [, ''feature-tag-value'' ]*</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197161 CSS 3 Fonts], Section 6.12
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
|Topic_clusters=Fonts
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}