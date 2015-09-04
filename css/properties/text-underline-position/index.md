---
title: text-underline-position
tags:
  - CSS
  - Properties
readiness: 'Not Ready'
standardization_status: 'W3C Working Draft'
notes:
  - "\nDeletion Candidate:   This page is a candidate for deletion because the property was never implemented. To underline text, see http://docs.webplatform.org/wiki/css/properties/text-decoration.\n\n"
summary: "Unsupported.\n"
uri: css/properties/text-underline-position

---
# text-underline-position

## Summary

Unsupported.

This property will add a underline position value to the element that has an underline defined.

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
:   as specified
Animatable
:   No
[CSS Object Model Property](/css/concepts/cssom)
:   ``
Percentages
:   N/A

## Syntax

-   `text-underline-position: alphabetic`
-   `text-underline-position: auto`
-   `text-underline-position: left`
-   `text-underline-position: right`
-   `text-underline-position: under`

## Values

auto
:   Decoration appears above the text.

alphabetic
:   The underline is positioned relative to the alphabetic baseline. In this case the underline is likely to cross some descenders. Decoration appears below the text.

under
:   The underline is positioned under the element's text content. In this case the underline usually does not cross the descenders. (This is sometimes called "accounting" underline.) This value can be combined with ‘left’ or ‘right’ if a particular side is preferred in vertical writing modes.

left
:   In vertical writing modes, the underline is aligned as for ‘under’, except it is always aligned to the left edge of the text. If this causes the underline to be drawn on the "over" side of the text, then an overline also switches sides and is drawn on the "under" side.

right
:   In vertical writing modes, the underline is aligned as for ‘under’, except it is always aligned to the right edge of the text. If this causes the underline to be drawn on the "over" side of the text, then an overline also switches sides and is drawn on the "under" side.

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[CSS Text Decoration Module Level 3](http://www.w3.org/TR/css-text-decor-3/#text-underline-position-property)
:   Working Draft

## See also

### Related articles

#### Text

-   [block-progression](/css/properties/block-progression)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [font-synthesis](/css/properties/font-synthesis)

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

-   **text-underline-position**

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

### Related pages (MSDN)

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `runtimeStyle`
-   `style`
-   `CSS Text Level 3`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

