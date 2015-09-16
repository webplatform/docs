---
title: 'font-kerning'
code_samples:
  - 'http://gist.github.com/7283111'
compatibility:
  feature: font-kerning
  topic: css
notes:
  - 'Example provided is not effective, add compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'all elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`font`'
  Percentages: N/A
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The font-kerning property allows contextual adjustment of inter-glyph spacing, i.e. the spaces between the characters in text. This property  controls &lt;bold&gt;metric kerning&lt;/bold&gt; - that utilizes adjustment data contained in the font. Optical Kerning is not supported as yet.'
tags:
  - CSS
  - Properties
uri: css/properties/font-kerning

---
## Summary

The font-kerning property allows contextual adjustment of inter-glyph spacing, i.e. the spaces between the characters in text. This property controls &lt;bold&gt;metric kerning&lt;/bold&gt; - that utilizes adjustment data contained in the font. Optical Kerning is not supported as yet.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `auto`

Applies to
:   all elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `font`

Percentages
:   N/A

## Syntax

-   `font-kerning: auto`
-   `font-kerning: none`
-   `font-kerning: normal`

## Values

auto
:   Used to specify kerning is at the discretion of the user agent.

normal
:   Specifies kerning is applied. Fonts that do not include kerning data are unaffected by this setting.

none
:   Specifies kerning is not applied

## Examples

-   Kerning will only be visible when supported.

``` html
<p class="normal">WAVAWAVAWAVAWAVA</p>
<p class="none"    >WAVAWAVAWAVAWAVA</p>
```

[View live example](http://code.webplatform.org/gist/7283111)

-   Kerning will only be visible when supported.

``` css
html { font-size: 62.5%; }
p { font-family: "Arial", serif; font-size: 3.6rem }
p.normal {font-kerning: normal;}
p.none {font-kerning: none;}
```

[View live example](http://code.webplatform.org/gist/7283111)

## Usage

     In auto setting, user agents can determine whether to apply kerning or not based on a number of factors like text size, script, or other factors that influence text processing speed. Authors who what proper kerning should use 'normal' to explicitly enable kerning. Likewise, use none to explicitly disable kerning. There is a performance tradeoff when enabling kerning which might not have a large impact on text rendering speed for modern implementations.

## Notes

Kerning data is a must for this property to take effect. When rendering OpenType fonts, the opentype specification states that kerning be enabled by default. When kerning is enabled, the OpenType `kern` feature is enabled. `vkern` is used for vertical text. User Agents must also support kerning via data contained in a `kern` font table, as detailed in the OpenType specification. When used in conjunction with `letter-spacing`, kerning adjustments are considered part of the default spacing and letter spacing adjustments are made \<bold\>after\</bold\> kerning has been applied.

## Related specifications

[CSS Fonts Module Level 3](http://www.w3.org/TR/css-fonts-3/#font-kerning-prop)
:   W3C Candidate Recommendation

## See also

### Related articles

#### CSS Font

-   [font-family](/css/properties/font-family)

-   **font-kerning**

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [font-size-adjust](/css/properties/font-size-adjust)

-   [font-style](/css/properties/font-style)

-   [font-variant](/css/properties/font-variant)

-   [text-rendering](/css/properties/text-rendering)

-   [text-underline](/css/properties/text-underline)

-   [user-modify](/css/properties/user-modify)

#### Fonts

-   [@font-face](/css/atrules/@font-face)

-   [Font related properties](/css/fonts)

-   [font-variant](/css/fonts/font-variant)

-   [font](/css/properties/font)

-   [font-family](/css/properties/font-family)

-   [font-feature-settings](/css/properties/font-feature-settings)

-   **font-kerning**

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [font-size-adjust](/css/properties/font-size-adjust)

-   [font-stretch](/css/properties/font-stretch)

-   [font-style](/css/properties/font-style)

-   [font-variant](/css/properties/font-variant)

-   [user-modify](/css/properties/user-modify)

-   [size](/html/attributes/size)

-   [font](/html/elements/font)
