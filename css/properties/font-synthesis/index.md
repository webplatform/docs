---
title: font-synthesis
tags:
  - CSS
  - Properties
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'Add example, description, specifications, compatibility.'
summary: 'This value specifies whether the user agent is allowed to synthesize  bold or oblique font faces when a font family lacks bold or italic faces.'
uri: css/properties/font-synthesis

---
# font-synthesis

## Summary

This value specifies whether the user agent is allowed to synthesize bold or oblique font faces when a font family lacks bold or italic faces.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `weight style`
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

-   `font-synthesis: none`
-   `font-synthesis: style`
-   `font-synthesis: weight`
-   `font-synthesis: weight style`

## Values

none
:   user agent is not allowed to synthesize bold or oblique font when not available.

weight
:   user agent is only allowed to synthesize bold font when not available but not oblique.

style
:   user agent is only allowed to synthesize oblique font when not available but not bold.

weight style
:   user agent is allowed to synthesize both bold and oblique.

**Needs Examples**: This section should include examples.

## See also

### Related articles

#### CSS Font

-   [font-family](/css/properties/font-family)

-   [font-kerning](/css/properties/font-kerning)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [font-size-adjust](/css/properties/font-size-adjust)

-   [font-style](/css/properties/font-style)

-   **font-synthesis**

-   [font-variant](/css/properties/font-variant)

-   [kerning-mode](/css/properties/kerning-mode)

-   [kerning-pair-threshold](/css/properties/kerning-pair-threshold)

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

-   [font-kerning](/css/properties/font-kerning)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [font-size-adjust](/css/properties/font-size-adjust)

-   [font-stretch](/css/properties/font-stretch)

-   [font-style](/css/properties/font-style)

-   **font-synthesis**

-   [font-variant](/css/properties/font-variant)

-   [max-font-size](/css/properties/max-font-size)

-   [min-font-size](/css/properties/min-font-size)

-   [user-modify](/css/properties/user-modify)

-   [size](/html/attributes/size)

-   [font](/html/elements/font)

#### Text

-   [block-progression](/css/properties/block-progression)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   **font-synthesis**

-   [hanging-punctuation](/css/properties/hanging-punctuation)

-   [hyphenate-limit-chars](/css/properties/hyphenate-limit-chars)

-   [hyphenate-limit-lines](/css/properties/hyphenate-limit-lines)

-   [hyphenate-limit-zone](/css/properties/hyphenate-limit-zone)

-   [hyphens](/css/properties/hyphens)

-   [ime-mode](/css/properties/ime-mode)

-   [layout-flow](/css/properties/layout-flow)

-   [layout-grid](/css/properties/layout-grid)

-   [layout-grid-char](/css/properties/layout-grid-char)

-   [layout-grid-line](/css/properties/layout-grid-line)

-   [layout-grid-mode](/css/properties/layout-grid-mode)

-   [layout-grid-type](/css/properties/layout-grid-type)

-   [letter-spacing](/css/properties/letter-spacing)

-   [line-break](/css/properties/line-break)

-   [max-font-size](/css/properties/max-font-size)

-   [min-font-size](/css/properties/min-font-size)

-   [text-overflow-ellipsis](/css/properties/text-overflow-ellipsis)

-   [text-overflow-mode](/css/properties/text-overflow-mode)

-   [text-rendering](/css/properties/text-rendering)

-   [text-underline-position](/css/properties/text-underline-position)

-   [text-underline-style](/css/properties/text-underline-style)

-   [text-underline-width](/css/properties/text-underline-width)

-   [user-input](/css/properties/user-input)

-   [user-modify](/css/properties/user-modify)

-   [Text](/css/text)

-   [size](/html/attributes/size)

-   [b](/html/elements/b)

-   [b](/html/elements/b/ja)

-   [br](/html/elements/br)

-   [br](/html/elements/br/ja)

-   [caption](/html/elements/caption)

-   [cite](/html/elements/cite)

-   [code](/html/elements/code)

-   [del](/html/elements/del)

-   [dfn](/html/elements/dfn)

-   [em](/html/elements/em)

-   [font](/html/elements/font)

-   [hr](/html/elements/hr)

-   [i](/html/elements/i)

-   [ins](/html/elements/ins)

-   [kbd](/html/elements/kbd)

-   [mark](/html/elements/mark)

-   [samp](/html/elements/samp)

-   [strong](/html/elements/strong)

-   [Achieving typographic effects with the canvas tag](/tutorials/canvas_texteffects)

