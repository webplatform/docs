---
title: 'text-overline-style'
code_samples:
  - 'http://gist.github.com/7283917'
compatibility:
  feature: text-overline-style
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'all elements with and generated content with textual content'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value (except for initial and inherit)'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Specifies the line style for overline text decoration.'
tags:
  - CSS
  - Properties
uri: css/properties/text-overline-style

---
## Summary

Specifies the line style for overline text decoration.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `none`

Applies to
:   all elements with and generated content with textual content

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   specified value (except for initial and inherit)

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

## Syntax

-   `text-overline-style: dashed`
-   `text-overline-style: dot-dash`
-   `text-overline-style: dot-dot-dash`
-   `text-overline-style: dotted`
-   `text-overline-style: double`
-   `text-overline-style: none`
-   `text-overline-style: solid`
-   `text-overline-style: wave`

## Values

none
:   Produces no line.

solid
:   Produces a solid line.

double
:   Produces a double line.

dotted
:   Produces a dotted line.

dashed
:   Produces a dashed line style.

dot-dash
:   Produces a line whose repeating pattern is a dot followed by a dash.

dot-dot-dash
:   Produces a line whose repeating pattern is two dots followed by a dash.

wave
:   Produces a wavy line.

## Examples

Incomplete because no browser has implemented this property.

``` css
p {
  text-overline-style: wavy;
}
```

[View live example](http://code.webplatform.org/gist/7283917)

## Notes

Not implemented in any browser.

## Related specifications

[CSS3 Text Module](http://www.w3.org/TR/2003/CR-css3-text-20030514/#text-decoration-style)
:   Candidate Recommendation
