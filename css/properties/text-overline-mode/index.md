---
title: 'text-overline-mode'
code_samples:
  - 'http://code.webplatform.org/gist/7283851'
compatibility:
  feature: text-overline-mode
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`continuous`'
  'Applies to': 'all elements with and generated content with textual content'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value (except for initial and inherit)'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Sets the mode for the overline text decoration, determining whether the text decoration affects the space characters or not.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/text-overline-mode

---
## Summary

Sets the mode for the overline text decoration, determining whether the text decoration affects the space characters or not.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `continuous`

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

-   `text-overline-mode: continuous`
-   `text-overline-mode: skip-white-space`

## Values

continuous
:   This value means that the line is continuous.

skip-white-space
:   This means that space characters will not be lined.

## Examples

Currently not implemented in any browser, so example is incomplete.

``` css
p {
  text-overline-mode: skip-white-space;
}
```

[View live example](http://code.webplatform.org/gist/7283851)

## Notes

Not implemented in any browser, but Chrome has a placeholder property for it (which may fool any feature detectors into thinking it works).

## Related specifications

[CSS3 Text Module](http://www.w3.org/TR/2003/CR-css3-text-20030514/#text-decoration-mode)
:   Candidate Recommendation
