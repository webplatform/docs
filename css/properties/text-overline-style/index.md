---
title: text-overline-style
code_samples:
  - 'http://gist.github.com/7283917'
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
## <span>Summary</span>

Specifies the line style for overline text decoration.

## <span>Overview table</span>

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

## <span>Syntax</span>

-   `text-overline-style: dashed`
-   `text-overline-style: dot-dash`
-   `text-overline-style: dot-dot-dash`
-   `text-overline-style: dotted`
-   `text-overline-style: double`
-   `text-overline-style: none`
-   `text-overline-style: solid`
-   `text-overline-style: wave`

## <span>Values</span>

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

## <span>Examples</span>

Incomplete because no browser has implemented this property.

``` css
p {
  text-overline-style: wavy;
}
```

[View live example](http://code.webplatform.org/gist/7283917)

## <span>Notes</span>

Not implemented in any browser.

## <span>Related specifications</span>

[CSS3 Text Module](http://www.w3.org/TR/2003/CR-css3-text-20030514/#text-decoration-style)
:   Candidate Recommendation
