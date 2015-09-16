---
title: padding-top
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/).'
  - 'Microsoft Developer Network.'
code_samples:
  - 'http://gist.github.com/6948436'
  - 'http://gist.github.com/6948429'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`0`'
  'Applies to': 'all elements (except table-\*-group, table-row and table-column, br)'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'the percentage as specified or the absolute length'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: '[[CSS percentages::refer to [width](/css/properties/width) of closest block-level ancestor]]'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The padding-top CSS property of an element sets the padding space required on the top of an element. The padding area is the space between the content of the element and its border. Contrary to margin-top values, negative values of padding-top are invalid.'
tags:
  - CSS
  - Properties
uri: css/properties/padding-top

---
## Summary

The padding-top CSS property of an element sets the padding space required on the top of an element. The padding area is the space between the content of the element and its border. Contrary to margin-top values, negative values of padding-top are invalid.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `0`

Applies to
:   all elements (except table-\*-group, table-row and table-column, br)

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

## Syntax

-   `padding-top: length`
-   `padding-top: percentage`

## Values

length
:   Specifies a positive fixed distance. See [length](/css/data_types/length) for details.

percentage
:   A percentage with respect to the height of the containing block.

## Examples

The following examples use the **padding-top** property to change the padding of the elements.

``` css
td { padding-top: 20%; }
```

[View live example](http://code.webplatform.org/gist/6948436)

``` css
td { padding-top: 30px; }
```

[View live example](http://code.webplatform.org/gist/6948429)

### Syntax

`padding-top:  <length>  |  <percentage>`

## Related specifications

[CSS basic box model](http://www.w3.org/TR/css3-box/)
:   W3C Working Draft

[CSS 2.1, 8 Box model](http://www.w3.org/TR/CSS21/box.html#propdef-padding)
:   W3C Recommendation
