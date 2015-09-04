---
title: font-variant
tags:
  0: CSS
  1: Properties
  3: Design
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
notes:
  - "\nMerge Candidate:  This page is a candidate for merge with the following pages: /css/properties/font-variant \n\n"
summary: 'Selects a normal, or small-caps face from a font family. Also possible by using the font shorthand.'
code_samples:
  - 'http://gist.github.com/5716625'
uri: css/fonts/font-variant
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - css/fonts/font-variant/css/properties/font-variant
    - dom/defaultSelected

---
# font-variant

## Summary

Selects a normal, or small-caps face from a font family. Also possible by using the font shorthand.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `normal`
Applies to
:   All elements
[Inherited](/css/concepts/inherited)
:   yes
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   As specified
Animatable
:   no
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
:   Default. Specifies a normal font face.

small-caps
:   Specifies a small-caps labeled font. If no small-case font is available, some browser (e.g. Firefox) simulate a small-case font by replacing the lowercase characters by scaled uppercase letters.

inherit
:   Inherit to the parent element.

## Examples

A simple example to show the effect achieved when small-caps are applied to a text paragraph

``` {.html}
I think WebPlatform rocks
```

[View live example](http://code.webplatform.org/gist/5716625)

The CSS applied to the HTML above.

``` {.css}
p {
  font-variant: small-caps;
}
```

## Related specifications

Specification
:   Status
[CSS 3](http://www.w3.org/TR/css3-fonts/#font-variant-prop)
:   W3C Candidate Recommendation
[CSS 2.1](http://www.w3.org/TR/CSS21/fonts.html#small-caps)
:   W3C Recommendation

## See also

### Related articles

#### Fonts

-   [@font-face](/css/atrules/@font-face)

-   [Font related properties](/css/fonts)

-   **font-variant**

-   [font](/css/properties/font)

-   [font-family](/css/properties/font-family)

-   [font-feature-settings](/css/properties/font-feature-settings)

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

### Related pages (MSDN)

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `defaults`
-   `runtimeStyle`
-   `style`
-   `font`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

