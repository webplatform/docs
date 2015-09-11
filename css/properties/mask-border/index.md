---
title: mask-border
notes:
  - "Add description and compatibility.\nAs of time of writing, this property is not yet implemented in most browsers."
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`See individual properties.`'
  'Applies to': 'See individual properties.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'See individual properties.'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: 'See individual properties.'
readiness: 'In Progress'
standardization_status: 'W3C Last Call Working Draft'
summary: 'This property is shorthand for setting mask-border-source, mask-border-slice, mask-border-width, mask-border-outset, and mask-border-repeat. Omitted values are set to their original properties'' initial values.'
tags:
  - CSS
  - Properties
uri: css/properties/mask-border

---
## <span>Summary</span>

This property is shorthand for setting mask-border-source, mask-border-slice, mask-border-width, mask-border-outset, and mask-border-repeat. Omitted values are set to their original properties' initial values.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `See individual properties.`

Applies to
:   See individual properties.

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   See individual properties.

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   See individual properties.

## <span>Syntax</span>

-   `mask-border: <mask-border-outset>`
-   `mask-border: <mask-border-repeat>`
-   `mask-border: <mask-border-slice>`
-   `mask-border: <mask-border-source>`
-   `mask-border: <mask-border-width>`

## <span>Values</span>

\<mask-border-source\>
:   See [mask-border-source](/css/properties/mask-border-source).

\<mask-border-slice\>
:   See [mask-border-slice](/css/properties/mask-border-slice).

\<mask-border-width\>
:   See [mask-border-width](/css/properties/mask-border-width).

\<mask-border-outset\>
:   See [mask-border-outset](/css/properties/mask-border-outset).

\<mask-border-repeat\>
:   See [mask-border-repeat](/css/properties/mask-border-repeat).

## <span>Examples</span>

``` css
/* mask-border-source (-slice) / -width / (-outset) -repeat */
#maskbox1 {
    mask-border: url(#someMask) / 5% / stretch;
}
```

## <span>Related specifications</span>

[CSS Masking Level 1](http://www.w3.org/TR/css-masking-1/)
:   W3C Last Call Working Draft

[CSS Masking Level 1](http://dev.w3.org/fxtf/css-masking-1/)
:   W3C Editor’s Draft
