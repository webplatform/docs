---
title: 'font-variant'
code_samples:
  - 'http://gist.github.com/5716625'
compatibility:
  feature: font-variant
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`normal`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`fontVariant`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The font-variant property enables you to select the small-caps font within a font family.'
tags:
  - CSS
  - Properties
uri: css/properties/font-variant

---
## Summary

The font-variant property enables you to select the small-caps font within a font family.

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
:   as specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `fontVariant`

Percentages
:   N/A

## Syntax

-   `font-variant: inherit`
-   `font-variant: normal`
-   `font-variant: small-caps`

## Values

normal
:   Selects a font that is not a 'small-caps' font, usually the available 'normal' font.

small-caps
:   Selects a 'small-caps' font. If not small caps variant is available, the browser generates a small caps approximation.

inherit
:   Inherits the font-variant setting from its parent.

## Examples

A simple example to show the effect achieved when small-caps are applied to a text paragraph.

``` html
<p>I think WebPlatform rocks.</p>
```

[View live example](http://code.webplatform.org/gist/5716625)

The CSS applied to the HTML above.

``` css
p {
  font-size: 300%;
  font-variant: small-caps;
}
```

## Notes

In ([CSS Fonts Module Level 3, W3C Working Draft 11 December 2012](http://www.w3.org/TR/css3-fonts/#propdef-font-variant)), this property is extended. However, no browser seems to support these changes yet.

## Related specifications

[CSS Fonts Module Level 3](http://www.w3.org/TR/css3-fonts/#propdef-font-variant)
:   W3C Candidate Recommendation

[Cascading Style Sheets Level 2 Revision 1 (CSS 2.1) Specification](http://www.w3.org/TR/CSS21/fonts.html#small-caps)
:   W3C Recommendation

## See also

### Related articles

#### CSS Font

-   [font-family](/css/properties/font-family)

-   [font-kerning](/css/properties/font-kerning)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [font-size-adjust](/css/properties/font-size-adjust)

-   [font-style](/css/properties/font-style)

-   **font-variant**

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

-   **font-variant**

-   [user-modify](/css/properties/user-modify)

-   [size](/html/attributes/size)

-   [font](/html/elements/font)

### External resources

-   MDN: [[1]](https://developer.mozilla.org/en-US/docs/Web/CSS/font-variant)
