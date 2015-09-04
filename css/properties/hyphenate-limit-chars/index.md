---
title: hyphenate-limit-chars
tags:
  - CSS
  - Properties
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
notes:
  - 'Add description, compatibility.'
summary: 'Specifies the minimum number of characters in a hyphenated word'
uri: css/properties/hyphenate-limit-chars

---
# hyphenate-limit-chars

## Summary

Specifies the minimum number of characters in a hyphenated word

## Overview table

[Initial value](/css/concepts/initial_value)
:   `auto`
Applies to
:   All elements
[Inherited](/css/concepts/inherited)
:   Yes
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   specified value
Animatable
:   No
[CSS Object Model Property](/css/concepts/cssom)
:   `hyphenateLimitChars`
Percentages
:   N/A

## Syntax

-   `hyphenate-limit-chars: integer`
-   `hyphenate-limit-chars: auto`

## Values

auto
:   Corresponds to a value of `5 2 2`, indicating a 5-character word limit, 2 characters required before a hyphenation break, and 2 characters required following a hyphenation break.

[integer](/css/data_types/integer)
:   One to three integer values, corresponding to the word limit, the minimum number of characters required before a hyphenation break, and the minimum number of characters required following a hyphenation break, respectively.

If the third value is missing it is equal to the second.

If the second and third values are missing they are given a value of **auto**.

Negative values are not allowed.

## Examples

``` {.css}
/* Only hyphenate words with >= 6 characters,
   leave at least 3 characters before the hyphen and at least 2 after it */
hyphenate-limit-chars: 6 3 2;
```

## Related specifications

Specification
:   Status
[CSS Text Level 4](http://dev.w3.org/csswg/css-text-4/#hyphenate-limit-chars)
:   W3C Editor’s Draft

## See also

### Related articles

#### Text

-   [block-progression](/css/properties/block-progression)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [font-synthesis](/css/properties/font-synthesis)

-   [hanging-punctuation](/css/properties/hanging-punctuation)

-   **hyphenate-limit-chars**

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

### Related pages

-   `CSSStyleDeclaration`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

