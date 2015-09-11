---
title: text-overline-mode
code_samples:
  - 'http://gist.github.com/7283851'
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
  - CSS
  - Properties
uri: css/properties/text-overline-mode

---
## <span>Summary</span>

Sets the mode for the overline text decoration, determining whether the text decoration affects the space characters or not.

## <span>Overview table</span>

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

## <span>Syntax</span>

-   `text-overline-mode: continuous`
-   `text-overline-mode: skip-white-space`

## <span>Values</span>

continuous
:   This value means that the line is continuous.

skip-white-space
:   This means that space characters will not be lined.

## <span>Examples</span>

Currently not implemented in any browser, so example is incomplete.

``` css
p {
  text-overline-mode: skip-white-space;
}
```

[View live example](http://code.webplatform.org/gist/7283851)

## <span>Notes</span>

Not implemented in any browser, but Chrome has a placeholder property for it (which may fool any feature detectors into thinking it works).

## <span>Related specifications</span>

[CSS3 Text Module](http://www.w3.org/TR/2003/CR-css3-text-20030514/#text-decoration-mode)
:   Candidate Recommendation
