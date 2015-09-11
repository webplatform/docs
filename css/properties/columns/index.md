---
title: columns
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/).'
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
code_samples:
  - 'http://gist.github.com/6288803'
notes:
  - 'Add description, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`See individual properties.`'
  'Applies to': 'Non-replaced block-level elements (except table elements), table cells, and inline-block elements.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'See individual properties.'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: 'See individual properties.'
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
summary: 'This property is a shorthand property for setting column-width and/or column-count.'
tags:
  - CSS
  - Properties
uri: css/properties/columns

---
## <span>Summary</span>

This property is a shorthand property for setting column-width and/or column-count.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `See individual properties.`

Applies to
:   Non-replaced block-level elements (except table elements), table cells, and inline-block elements.

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

-   `columns: column-count`
-   `columns: column-width`

## <span>Values</span>

column-width
:   Any of the values available to [column-width](/css/properties/column-width) property.

column-count
:   Any of the values available to [column-count](/css/properties/column-count) property.

## <span>Examples</span>

``` css
/* Make 3 columns at auto width */
#columns {
  columns: auto 3;
}
```

[View live example](http://code.webplatform.org/gist/6288803)

## <span>Related specifications</span>

[CSS Multi-column Layout Module](http://www.w3.org/TR/css3-multicol)
:   W3C Candidate Recommendation
