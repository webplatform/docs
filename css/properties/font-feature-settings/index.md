{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The <code>font-feature-settings</code> property gets or sets one or more values that specify glyph substitution and positioning in fonts that include OpenType layout features.}}
{{CSS Property
|Initial value=normal
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=As specified
|Animatable=No
|CSS object model property=fontFeatureSettings
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=normal
|Description=Default. No change in glyph substitution or positioning occurs.
}}{{CSS Property Value
|Data Type=OpenType feature tag, Indicator
|Description=* OpenType feature tag: Comma-separated list of one or more OpenType layout feature tags (each with an optional toggle). See [[css/properties/font-feature-settings#Notes|Notes]] for examples of correct syntax, plus a table of the most common feature tags and their definitions.
* Indicator: 0 indicates that the feature is disabled. For boolean features, 1 indicates that feature is enabled. A value of ‘on’ is synonymous with 1 and ‘off’ is synonymous with 0. For non-boolean features, 1 or greater indicates the feature selection index.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=OpenType specification defines many advanced typographic features that can be implemented by font designers. For instance, you can define vertical positioning for a font, substitute glyph forms with ligatures, contextual alternates, stylistic alternates, or swashes, include a set of small caps, and more.<br />
Each defined feature has a corresponding feature tag that identifies its function and effects. Font developers can also define their own features. A feature's tag determines what the feature does and whether to implement it. The following table lists some of the most common feature tags and their definitions.<br />
For the full list of OpenType layout features, see [http://go.microsoft.com/fwlink/p/?LinkId{{=}}236359 OpenType layout feature tag registry].

* <code>kern</code> — Kerning
* <code>smcp</code> — Small capitals
* <code>liga</code> — Standard ligatures
* <code>dlig</code> — Discretionary ligatures
* <code>ss01</code>, <code>ss02</code>, <code>ss03</code> ... <code>ss20</code> — Stylistic sets (font-specific)
* <code>swsh</code> — Swash
* <code>tnum</code> — Tabular figures
* <code>lnum</code> — Lining figures
* <code>onum</code> — Oldstyle figures

If you are unfamiliar with the font features listed above, the CSS Fonts Module Level 3 specification has good explanations and visual examples of each feature in Section 6, "[http://go.microsoft.com/fwlink/?LinkID{{=}}236360 Font feature properties]." Be aware that, though the properties listed correspond to OpenType layout features that might be supported, the properties themselves ('''font-kerning''', '''font-variant-*''', and so on) are not supported.


Whenever possible, Web authors should use the <code>font-variant</code> property. This property has been designed to handle special cases where no other way to enable or access an OpenType font feature does exists.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Fonts Module Level 3
|URL=http://www.w3.org/TR/css3-fonts/#propdef-font-feature-settings
|Status=W3C Working Draft
}}
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
|External_links=* Mozilla: [http://hacks.mozilla.org/2010/11/firefox-4-font-feature-support/ Firefox 4: OpenType font feature support]
* IEBlog: [https://blogs.msdn.com/b/ie/archive/2012/01/09/css-corner-using-the-whole-font.aspx?Redirected=true CSS Corner: Using the Whole Font]
* FontDeck blog: [http://blog.fontdeck.com/post/15777165734/opentype-1 Using OpenType font features with CSS 3]
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