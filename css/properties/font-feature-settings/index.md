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
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=16.0
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=4.0
|Internet_explorer_supported=Yes
|Internet_explorer_version=10.0
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=6.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=Yes
|Blackberry_prefixed_version=10.0
|Chrome_mobile_supported=No
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Yes
|Chrome_mobile_prefixed_version=18.0
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Yes
|Firefox_mobile_prefixed_version=18.0
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Firefox
|Version=From Gecko 2.0 (Firefox 4.0) to Gecko 14.0 (Firefox 14.0) included
|Note=Gecko supported an older syntax, slightly different from the modern one: [http://hacks.mozilla.org/2010/11/firefox-4-font-feature-support/ OpenType Font Feature support in Firefox 4].
}}{{Compatibility Notes Row
|Browser=Chrome
|Note=Partial support in older Chrome versions refers to lacking support in Mac OS X.
}}
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