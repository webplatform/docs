---
title: letter-spacing
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5671141'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`normal`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'normal or absolute length'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`letterSpacing`'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The letter-spacing CSS property specifies the spacing behavior between text characters.'
tags:
  - CSS
  - Properties
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected
uri: css/properties/letter-spacing

---
## Summary

The letter-spacing CSS property specifies the spacing behavior between text characters.

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
:   normal or absolute length

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `letterSpacing`

## Syntax

-   `letter-spacing: length`
-   `letter-spacing: normal`

## Values

normal
:   The spacing is the normal spacing for the current font.

length
:   Indicates inter-character space in addition to the default space between characters, followed by an absolute units designator (cm, mm, in, pt, or pc) or a relative units designator (em, ex, or px). Values may be negative, but there may be implementation-specific limits.

## Examples

A selection of examples showing some typical uses of the letter-spacing property.

``` html
<p>This is a simple paragraph with the default value for letter-spacing.</p>

<p class="pos">This is a simple paragraph with a altered letter-spacing value by 0.3em.</p>

<p class="neg">This is a simple paragraph withe a altered letter-spacing value by -0.1em</p>
```

[View live example](http://code.webplatform.org/gist/5671141)

``` css
p {
    letter-spacing: normal;
}

p.pos {
    letter-spacing: .3em;
}

p.neg {
    letter-spacing: -.1em;
}
```

## Usage

     * Up to three different values can be specified, in the following order: optimum, minimum, maximum

-   If one value is specified, it is used for all spacing. If two values are specified, the first is used for the optimum and minimum spacings, and the second is used for maximum.

## Notes

When specified as a positive **length** value, the **letter-spacing** attribute adds the specified value to the default spacing between characters within an element. A negative **length** value decreases the space between characters. Letter spacing can be influenced by justification.

## Related specifications

[CSS Text Module Level 3](http://www.w3.org/TR/css3-text/#letter-spacing)
:   W3C Working Draft

## See also

### Related articles

#### Text

-   [block-progression](/css/properties/block-progression)

-   [font-language-override](/css/properties/font-language-override)

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

-   **letter-spacing**

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

### Other articles

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `defaults`
-   `runtimeStyle`
-   `style`
