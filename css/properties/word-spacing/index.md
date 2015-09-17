---
title: 'word-spacing'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5671391'
compatibility:
  feature: word-spacing
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`normal`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'an optimum, minimum, and maximum value, each consisting of either an absolute length, a percentage, or the keyword ‘normal’'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`wordSpacing`'
  Percentages: 'refers to width of the affected glyph'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The word-spacing CSS property specifies the spacing behavior between &quot;words&quot;.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/word-spacing

---
## Summary

The word-spacing CSS property specifies the spacing behavior between &quot;words&quot;.

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
:   an optimum, minimum, and maximum value, each consisting of either an absolute length, a percentage, or the keyword ‘normal’

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `wordSpacing`

Percentages
:   refers to width of the affected glyph

## Syntax

-   `word-spacing: length`
-   `word-spacing: normal`
-   `word-spacing: percentage`

## Values

normal
:   The spacing is the normal spacing for the current font.

length
:   Indicates inter-word space in addition to the default space between words, followed by an absolute units designator (cm, mm, in, pt, or pc) or a relative units designator (em, ex, or px). Values may be negative, but there may be implementation-specific limits.

percentage
:   Specifies the additional spacing as a percentage of the affected word's advance measure.

## Examples

The following example shows how to use the **word-spacing** attribute and the **word-spacing** property to increase the amount of space between words in a `p` element.

``` html
<p>This is a simple paragraph with the default value for word-spacing.</p>

<p class="pos">This is a simple paragraph with a altered word-spacing value by 0.3em.</p>

<p class="neg">This is a simple paragraph withe a altered word-spacing value by -0.1em</p>
```

[View live example](http://gist.github.com/5671391)

``` css
p {
    word-spacing: normal;
}

p.pos {
    word-spacing: .3em;
}

p.neg {
    word-spacing: -.1em;
}
```

## Usage

     * Up to three different values can be specified, in the following order: optimum, minimum, maximum

-   If one value is specified, it is used for all spacing. If two values are specified, the first is used for the optimum and minimum spacings, and the second is used for maximum.

## Notes

When specified as a positive `length` value, the `word-spacing` attribute adds the specified value to the default spacing between words within an element. A negative `length` value decreases the space between words. Word spacing can be influenced by justification.

## Related specifications

[CSS Text Module Level 3](http://www.w3.org/TR/css3-text/#word-spacing)
:   W3C Working Draft

## See also

### Other articles

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
-   `CSS Enhancements in Internet Explorer 6`
