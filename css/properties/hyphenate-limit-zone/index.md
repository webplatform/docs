---
title: 'hyphenate-limit-zone'
compatibility:
  feature: hyphenate-limit-zone
  topic: css
notes:
  - 'Add description, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`0`'
  'Applies to': 'block containers'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`hyphenateLimitZone`'
  Percentages: 'refer to width of the line box'
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
summary: 'Specifies the maximum amount of trailing whitespace (before justification) that may be left in a line before hyphenation is triggered to pull part of a word from the next line back up into the current one.'
tags:
  - CSS
  - Properties
uri: css/properties/hyphenate-limit-zone

---
## Summary

Specifies the maximum amount of trailing whitespace (before justification) that may be left in a line before hyphenation is triggered to pull part of a word from the next line back up into the current one.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `0`

Applies to
:   block containers

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   specified value

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `hyphenateLimitZone`

Percentages
:   refer to width of the line box

## Syntax

-   `hyphenate-limit-zone: length`
-   `hyphenate-limit-zone: percentage`

## Values

percentage
:   Specifies the width of the hyphenation zone, relative to the total line length. Negative values are not allowed.

length
:   Indicates the width of the hyphenation zone. Lengths set in font-relative units (em, ex, ch) tend to be more useful here. Negative values are not allowed.

## Examples

``` css
/* Only hyphenate if the line would otherwise be <= 90% its maximum possible width */
hyphenate-limit-zone: 10%;
```

## Related specifications

[CSS Text Level 4](http://dev.w3.org/csswg/css-text-4/#hyphenate-limit-zone)
:   W3C Editor’s Draft

## See also

### Related articles

#### Text

-   [block-progression](/css/properties/block-progression)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [hyphenate-limit-chars](/css/properties/hyphenate-limit-chars)

-   [hyphenate-limit-lines](/css/properties/hyphenate-limit-lines)

-   **hyphenate-limit-zone**

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
