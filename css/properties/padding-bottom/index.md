---
title: padding-bottom
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/).'
code_samples:
  - 'http://gist.github.com/6948355'
  - 'http://gist.github.com/6948398'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`0`'
  'Applies to': 'All elements (except table-\*-group, table-row and table-column, br)'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'the percentage as specified or the absolute length'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: '[[CSS percentages::refer to [width](/css/properties/width) of closest block-level ancestor]]'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The padding-bottom CSS property of an element sets the padding space required on the bottom of an element. The padding area is the space between the content of the element and its border. Contrary to margin-bottom values, negative values of padding-bottom are invalid.'
tags:
  - CSS
  - Properties
uri: css/properties/padding-bottom

---
## <span>Summary</span>

The padding-bottom CSS property of an element sets the padding space required on the bottom of an element. The padding area is the space between the content of the element and its border. Contrary to margin-bottom values, negative values of padding-bottom are invalid.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `0`

Applies to
:   All elements (except table-\*-group, table-row and table-column, br)

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   the percentage as specified or the absolute length

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   [[CSS percentages::refer to [width](/css/properties/width) of closest block-level ancestor]]

## <span>Syntax</span>

-   `padding-bottom: length`
-   `padding-bottom: percentage`

## <span>Values</span>

length
:   Specifies a positive fixed distance. See [length](/css/data_types/length) for details.

percentage
:   Calculated using the dimensions of the containing block or element.

## <span>Examples</span>

The following examples use the `padding-bottom` property to change the [padding](/css/properties/padding) of the elements.

``` css
td { padding-bottom: 20%; }
```

[View live example](http://code.webplatform.org/gist/6948355)

``` css
td { padding-bottom: 30px; }
```

[View live example](http://code.webplatform.org/gist/6948398)

## <span>Related specifications</span>

[CSS basic box model](http://www.w3.org/TR/css3-box/)
:   W3C Working Draft

[CSS 2.1, 8 Box model](http://www.w3.org/TR/CSS21/box.html#propdef-padding)
:   W3C Recommendation
