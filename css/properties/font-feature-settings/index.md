---
title: font-feature-settings
tags:
  - CSS
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The font-feature-settings property gets or sets one or more values that specify glyph substitution (special font characters such as ligatures and figures) and positioning in fonts that include OpenType layout features.'
uri: css/properties/font-feature-settings

---
# font-feature-settings

## Summary

The font-feature-settings property gets or sets one or more values that specify glyph substitution (special font characters such as ligatures and figures) and positioning in fonts that include OpenType layout features.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `normal`
Applies to
:   All elements
[Inherited](/css/concepts/inherited)
:   Yes
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   As specified
Animatable
:   No
[CSS Object Model Property](/css/concepts/cssom)
:   `fontFeatureSettings`
Percentages
:   N/A

## Syntax

-   `font-feature-settings: "OpenType feature tag" Indicator`
-   `font-feature-settings: normal`

## Values

normal
:   Default. No change in glyph substitution or positioning occurs.

"OpenType feature tag" Indicator
:   This property can take up to two separate parts in its value. The options are as follows:

-   **OpenType feature tag**: Comma-separated list of one or more OpenType layout feature tags (each with an optional toggle). See [Notes](/css/properties/font-feature-settings#Notes) for examples of correct syntax, plus a table of the most common feature tags and their definitions.
-   **Indicator**: 0 indicates that the feature is disabled. For boolean features, 1 indicates that feature is enabled. A value of ‘on’ is synonymous with 1 and ‘off’ is synonymous with 0. For non-boolean features, 1 or greater indicates the feature selection index.

## Examples

A selection of examples showing some typical uses of the font-feater-settings property.

``` {.html}
<p class="smallcaps">Small caps</p>

<p class="ligatures">Ligatures</p>
```

``` {.css}
@font-face {
    font-family: 'myMinion';
    src: url('MinionPro-Regular.otf') format('opentype');
}

body {
    font-family: myMinion;
}

p.smallcaps { font-feature-settings: "smcp" 1; }

p.ligatures{ font-feature-settings: "liga" on; }
```

## Notes

OpenType specification defines many advanced typographic features that can be implemented by font designers. For instance, you can define vertical positioning for a font, substitute glyph forms with ligatures, contextual alternates, stylistic alternates, or swashes, include a set of small caps, and more.
 Each defined feature has a corresponding feature tag that identifies its function and effects. Font developers can also define their own features. A feature's tag determines what the feature does and whether to implement it. The following table lists some of the most common feature tags and their definitions.
 For the full list of OpenType layout features, see [OpenType layout feature tag registry](http://go.microsoft.com/fwlink/p/?LinkId=236359).

-   `kern` — Kerning
-   `smcp` — Small capitals
-   `liga` — Standard ligatures
-   `dlig` — Discretionary ligatures
-   `ss01`, `ss02`, `ss03` ... `ss20` — Stylistic sets (font-specific)
-   `swsh` — Swash
-   `tnum` — Tabular figures
-   `lnum` — Lining figures
-   `onum` — Oldstyle figures

If you are unfamiliar with the font features listed above, the CSS Fonts Module Level 3 specification has good explanations and visual examples of each feature in Section 6, "[Font feature properties](http://go.microsoft.com/fwlink/?LinkID=236360)." Be aware that, though the properties listed correspond to OpenType layout features that might be supported, the properties themselves (**font-kerning**, **font-variant-\***, and so on) are not supported.

 Whenever possible, Web authors should use the `font-variant` property. This property has been designed to handle special cases where no other way to enable or access an OpenType font feature exists.

## Related specifications

Specification
:   Status
[CSS Fonts Module Level 3](http://www.w3.org/TR/css3-fonts/#propdef-font-feature-settings)
:   W3C Working Draft

## See also

### Related articles

#### Fonts

-   [@font-face](/css/atrules/@font-face)

-   [Font related properties](/css/fonts)

-   [font-variant](/css/fonts/font-variant)

-   [font](/css/properties/font)

-   [font-family](/css/properties/font-family)

-   **font-feature-settings**

-   [font-kerning](/css/properties/font-kerning)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [font-size-adjust](/css/properties/font-size-adjust)

-   [font-stretch](/css/properties/font-stretch)

-   [font-style](/css/properties/font-style)

-   [font-synthesis](/css/properties/font-synthesis)

-   [font-variant](/css/properties/font-variant)

-   [max-font-size](/css/properties/max-font-size)

-   [min-font-size](/css/properties/min-font-size)

-   [user-modify](/css/properties/user-modify)

-   [size](/html/attributes/size)

-   [font](/html/elements/font)

### External resources

-   Mozilla: [Firefox 4: OpenType font feature support](http://hacks.mozilla.org/2010/11/firefox-4-font-feature-support/)
-   IEBlog: [CSS Corner: Using the Whole Font](https://blogs.msdn.com/b/ie/archive/2012/01/09/css-corner-using-the-whole-font.aspx?Redirected=true)
-   FontDeck blog: [Using OpenType font features with CSS 3](http://blog.fontdeck.com/post/15777165734/opentype-1)
-   Mozilla font-feature-settings: [[1]](https://developer.mozilla.org/en-US/docs/Web/CSS/font-feature-settings)
-   More info on font special characters (glyphs substitutions): [[2]](http://www.typography.com/fonts/hoefler-text/features/hoefler-text-special-characters)

### Related pages (MSDN)

-   `CSSStyleDeclaration`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

