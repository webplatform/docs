---
title: font-stretch
tags:
  - CSS
  - Properties
readiness: 'In Progress'
notes:
  - 'Add description and compatibility.'
summary: 'Allows you to expand or condense the widths for a normal, condensed, or expanded font face.'
code_samples:
  - 'http://gist.github.com/5842671'
uri: css/properties/font-stretch
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected

---
# font-stretch

## Summary

Allows you to expand or condense the widths for a normal, condensed, or expanded font face.

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
:   ``

## Syntax

-   `font-stretch: condensed`
-   `font-stretch: expanded`
-   `font-stretch: extra-condensed`
-   `font-stretch: extra-expanded`
-   `font-stretch: narrower (Internet Explorer only)`
-   `font-stretch: normal`
-   `font-stretch: semi-condensed`
-   `font-stretch: semi-expanded`
-   `font-stretch: ultra-condensed`
-   `font-stretch: ultra-expanded`
-   `font-stretch: wider (Internet Explorer only)`

## Values

ultra-condensed
:   This is the most condensed setting.

extra-condensed
:   This is the second most condensed setting.

condensed
:   Some font faces incorporate a condensed option, this is the equivalent of that setting.

semi-condensed
:   This is the least condensed setting.

normal
:   This is the default setting.

semi-expanded
:   This is the least expanded setting.

expanded
:   Some font faces incorporate an expanded option, this is the equivalent of that setting.

extra-expanded
:   This is the second most expanded setting.

ultra-expanded
:   This is the most expanded setting.

wider (Internet Explorer only)
:   This expands the font face in Internet Explorer only.

narrower (Internet Explorer only)
:   This condenses the font face in Internet Explorer only.

## Examples

``` {.css}
.ultra-condensed{
    font-stretch:ultra-condensed;
    }
.condensed{
    font-stretch:condensed;
    }
.normal{
    font-stretch:normal;
    }
.expanded{
    font-stretch:expanded;
    }
.ultra-expanded{
    font-stretch:ultra-expanded;
    }
```

[View live example](http://code.webplatform.org/gist/5842671)

### Syntax

`font-stretch: normal | wider | narrower | ultra-condensed | extra-condensed | condensed | semi-condensed | semi-expanded | expanded | extra-expanded | ultra-expanded `

### Standards information

-   [Scalable Vector Graphics: Text](http://go.microsoft.com/fwlink/p/?linkid=199818), Section 10.10

## See also

### Related articles

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

-   **font-stretch**

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
-   `LayoutRect`
-   `runtimeStyle`
-   `style`
-   `style`
-   `font-size-adjust`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

