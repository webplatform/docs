---
title: 'text-emphasis'
code_samples:
  - 'http://gist.github.com/6133067'
compatibility:
  feature: text-emphasis
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': none
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`textEmphasis`'
  Percentages: 'Not available'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The text-emphasis property will apply special emphasis marks to the elements text. Slightly similar to the text-decoration property only that this property can have affect on the line-height. It also is noted that this is shorthand for text-emphasis-style and for text-emphasis-color.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/text-emphasis

---
## Summary

The text-emphasis property will apply special emphasis marks to the elements text. Slightly similar to the text-decoration property only that this property can have affect on the line-height. It also is noted that this is shorthand for text-emphasis-style and for text-emphasis-color.

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
:   none

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `textEmphasis`

Percentages
:   Not available

## Syntax

-   `text-emphasis: <string>`
-   `text-emphasis: circle`
-   `text-emphasis: dot`
-   `text-emphasis: double-circle`
-   `text-emphasis: filled`
-   `text-emphasis: none`
-   `text-emphasis: open`
-   `text-emphasis: sesame`
-   `text-emphasis: triangle`

## Values

none
:   There are no emphasis marks

filled
:   It is filled with a solid color

open
:   The shape has an empty space

dot
:   Displays small circles as marks

circle
:   Displays large circles as marks

double-circle
:   Displays double circles as marks

triangle
:   Displays triangles as marks

sesame
:   Displays sesames as marks

\<string\>
:   Display the given string as marks. Authors should not specify more than one character in \<string\>. The UA may truncate or ignore strings consisting of more than one grapheme cluster.

## Examples

``` css
p {
  /*text-emphasis: shape color;*/
  text-emphasis: triangle #f70;
}
```

[View live example](http://gist.github.com/6133067)

``` css
p {
  /*text-emphasis: "string";*/
  text-emphasis: "*";
}
```

``` css
p {
  /*text-emphasis: "string" color;*/
  text-emphasis: "^" #ccc;
}
```

## Notes

Don't apply on special word separators like spaces.

Size of the marks will always scale to 50% of the container's actual font size.

## Related specifications

[CSS Text Decoration Module Level 3](http://dev.w3.org/csswg/css-text-decor-3/#emphasis-marks)
:   Editor's Draft
