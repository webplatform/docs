---
title: 'font-language-override'
compatibility:
  feature: font-language-override
  topic: css
notes:
  - 'Add example, specifications, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`normal`'
  'Applies to': 'all elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`font`'
  Percentages: N/A
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The ‘font-language-override’ property allows authors to explicitly specify the language system of the font, overriding the language system implied by the content language.'
tags:
  - CSS
  - Properties
uri: css/properties/font-language-override

---
## Summary

The ‘font-language-override’ property allows authors to explicitly specify the language system of the font, overriding the language system implied by the content language.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `normal`

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

-   `font-language-override: <string>`
-   `font-language-override: normal`

## Values

normal
:   specifies that when rendering with OpenType fonts, the content language of the element is used to infer the OpenType language system

\<string\>
:   single three-letter case-sensitive OpenType language system tag, specifies the OpenType language system to be used instead of the language system implied by the language of the element

**Needs Examples**: This section should include examples.

## Usage

     OpenType supports language-specific glyph selection and positioning, so that text can be displayed correctly in cases where the language dictates a specific display behavior. Authors can control the use of language-specific glyph substitutions and positioning by setting the content language of an element.

`<!-- Display text using S'gaw Karen specific features --> <p lang="ksw">...</p>`

## Notes

Use of invalid OpenType language system tags must not generate a parse error but must be ignored when doing glyph selection and placement.

## See also

### Related articles

#### CSS Font

-   [font-family](/css/properties/font-family)

-   [font-kerning](/css/properties/font-kerning)

-   **font-language-override**

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

-   [font-kerning](/css/properties/font-kerning)

-   **font-language-override**

-   [font-size](/css/properties/font-size)

-   [font-size-adjust](/css/properties/font-size-adjust)

-   [font-stretch](/css/properties/font-stretch)

-   [font-style](/css/properties/font-style)

-   [font-variant](/css/properties/font-variant)

-   [user-modify](/css/properties/user-modify)

-   [size](/html/attributes/size)

-   [font](/html/elements/font)

#### Text

-   [block-progression](/css/properties/block-progression)

-   **font-language-override**

-   [font-size](/css/properties/font-size)

-   [hyphenate-limit-chars](/css/properties/hyphenate-limit-chars)

-   [hyphenate-limit-lines](/css/properties/hyphenate-limit-lines)

-   [hyphenate-limit-zone](/css/properties/hyphenate-limit-zone)

-   [hyphens](/css/properties/hyphens)

-   [ime-mode](/css/properties/ime-mode)

-   [layout-grid](/css/properties/layout-grid)

-   [layout-grid-char](/css/properties/layout-grid-char)

-   [layout-grid-line](/css/properties/layout-grid-line)

-   [layout-grid-mode](/css/properties/layout-grid-mode)

-   [layout-grid-type](/css/properties/layout-grid-type)

-   [letter-spacing](/css/properties/letter-spacing)

-   [text-overflow-ellipsis](/css/properties/text-overflow-ellipsis)

-   [text-overflow-mode](/css/properties/text-overflow-mode)

-   [text-rendering](/css/properties/text-rendering)

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

### External resources

[Microsoft OpenType Layout Tag Registry](http://www.microsoft.com/typography/otspec/languagetags.htm)
