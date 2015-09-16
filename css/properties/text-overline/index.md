---
title: 'text-overline'
compatibility:
  feature: text-overline
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`not defined for shorthand properties`'
  'Applies to': 'all elements with and generated content with textual content'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The text-overline property is the shorthand for the text-overline-style, text-overline-width, text-overline-color, and text-overline-mode properties.'
tags:
  - CSS
  - Properties
uri: css/properties/text-overline

---
## Summary

The text-overline property is the shorthand for the text-overline-style, text-overline-width, text-overline-color, and text-overline-mode properties.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `not defined for shorthand properties`

Applies to
:   all elements with and generated content with textual content

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   N/A

## Syntax

-   `text-overline: <'text-overline-color'>`
-   `text-overline: <'text-overline-mode'>`
-   `text-overline: <'text-overline-style'>`

## Values

\<'text-overline-style'\>
:   Possible values:

None- Produces no line. solid - Produces a solid line. double - Produces a double line. dotted - Produces a dotted line. dashed - Produces a dashed line style. dot-dash - Produces a line whose repeating pattern is a dot followed by a dash. dot-dot-dash - Produces a line whose repeating pattern is two dots followed by a dash. wave - Produces a wavy line.

\<'text-overline-color'\>
:   Possible values:

\<color\> - Specifies a color value.

\<'text-overline-mode'\>
:   This property determines whether only words meant to be overlined or if the whitespace between words and words meant to be overlined. There are two unique values: continuous or words.

Continuous is the default value and shows overline for both words and whitespaces. Words only shows onverline for words and not whitespaces. It can also have the values of initial or inherit.

## Examples

Produces a single, solid, blue overline.

``` css
p {
   text-overline: solid blue;
}
```

## Related specifications

[CSS3 Text Module](http://www.w3.org/TR/2003/CR-css3-text-20030514/)
:   Candidate Recommendation
