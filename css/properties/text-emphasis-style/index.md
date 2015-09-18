---
title: 'text-emphasis-style'
code_samples:
  - 'http://code.webplatform.org/gist/6133332'
compatibility:
  feature: text-emphasis-style
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': '‘none’, a pair of keywords representing the shape and fill, or a string'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`textEmphasisStyle`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The text-emphasis-style property applies special emphasis marks to an element''s text.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/text-emphasis-style

---
## Summary

The text-emphasis-style property applies special emphasis marks to an element's text.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `none`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   ‘none’, a pair of keywords representing the shape and fill, or a string

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `textEmphasisStyle`

Percentages
:   N/A

## Syntax

-   `text-emphasis-style: <string>`
-   `text-emphasis-style: circle`
-   `text-emphasis-style: dot`
-   `text-emphasis-style: double-circle`
-   `text-emphasis-style: filled`
-   `text-emphasis-style: none`
-   `text-emphasis-style: open`
-   `text-emphasis-style: sesame`
-   `text-emphasis-style: triangle`

## Values

none
:   No emphasis marks.

filled
:   The shape is filled with solid color.

open
:   The shape is hollow.

dot
:   Display small circles as marks. The filled dot is U+2022 ‘•’, and the open dot is U+25E6 ‘◦’.

circle
:   Display large circles as marks. The filled circle is U+25CF ‘●’, and the open circle is U+25CB ‘○’.

double-circle
:   Display double circles as marks. The filled double-circle is U+25C9 ‘◉’, and the open double-circle is U+25CE ‘◎’.

triangle
:   Display triangles as marks. The filled triangle is U+25B2 ‘▲’, and the open triangle is U+25B3 ‘△’.

sesame
:   Display sesames as marks. The filled sesame is U+FE45 ‘﹅’, and the open sesame is U+FE46 ‘﹆’.

\<string\>
:   Display the given string as marks. Authors should not specify more than one character in \<string\>. The UA may truncate or ignore strings consisting of more than one grapheme cluster.

## Examples

``` css
p {
  /*text-emphasis-style: shape;*/
  text-emphasis-style: dot;
}
```

[View live example](http://code.webplatform.org/gist/6133332)

``` css
p {
  /*text-emphasis-style: <string>;*/
  text-emphasis-style: "^";
}
```

## Related specifications

[CSS Text Decoration Module Level 3](http://www.w3.org/TR/css-text-decor-3/)
:   W3C Candidate Recommendation
