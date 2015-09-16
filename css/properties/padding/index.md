---
title: 'padding'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/).'
  - 'Microsoft Developer Network.'
code_samples:
  - 'http://gist.github.com/5842631'
compatibility:
  feature: padding
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`browser-dependent`'
  'Applies to': 'all elements (except table-\*-group, table-row and table-column, br)'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'the percentage or the absolute length'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: 'relative to the ''width'' of the containing block'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: "The padding optional CSS property sets the required padding space on one to four sides of an element. The padding area is the space between an element and its border. Negative values are not allowed but decimal values are permitted.  The element size is treated as fixed, and the content of the element shifts toward the center as padding is increased.\n"
tags:
  - CSS
  - Properties
uri: css/properties/padding

---
## Summary

The padding optional CSS property sets the required padding space on one to four sides of an element. The padding area is the space between an element and its border. Negative values are not allowed but decimal values are permitted. The element size is treated as fixed, and the content of the element shifts toward the center as padding is increased.

The `padding` property is a shorthand to avoid setting each side separately ([padding-top](/css/properties/padding-top), [padding-right](/css/properties/padding-right), [padding-bottom](/css/properties/padding-bottom), [padding-left](/css/properties/padding-left)).

## Overview table

[Initial value](/css/concepts/initial_value)
:   `browser-dependent`

Applies to
:   all elements (except table-\*-group, table-row and table-column, br)

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   the percentage or the absolute length

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   relative to the 'width' of the containing block

## Syntax

-   `padding: length`
-   `padding: percentage`

## Values

length
:   Specifies a non-negative fixed width defined in pixels, pt, em, etc. . See [length](/css/data_types/length) for details.

percentage
:   Calculated using the dimensions of the containing block or element.

## Examples

Padding set at 10% for all 4 sides.

``` css
padding: 10% 10% 10% 10%;
      /*  top, right, bottom, and left padding set at 10%   */
```

[View live example](http://code.webplatform.org/gist/5842631)

The padding style has three values. The left padding value is the inferred by the right padding value.

``` css
padding: 10px 3% 20px;
      /*  top 10px padding          */
      /*  left and right 3% padding */
      /*  bottom 20px padding       */
```

The padding style has two values. The left padding value is the inferred by the right padding value. The bottom value is inferred by the top value.

``` css
padding: 10px 20%;
      /*  top and bottom 10px padding  */
       /*  left and right 20% padding  */
```

The padding style has one value. All the values are inferred to be equal to the top padding value of 10 px.

``` css
padding: 10px;
       /* on all sides 10px padding */
```

The padding style has one value. All the values are inferred to be equal to the top padding value of 20%.

``` css
padding: 20%;
       /* on all sides 20% padding */
```

## Notes

This is a composite property that specifies up to four padding values, in the following order: top, right, bottom, left. If one width value is specified, it is used for all four sides. If two width values are specified, the first is used for the top and bottom borders, and the second is used for left and right borders. If three width values are specified, they are used for top, right/left, and bottom borders, respectively. Negative values are not allowed.

As of Microsoft Internet Explorer 5.5, this property applies to inline elements. With earlier versions of Windows Internet Explorer, inline elements must have an **absolute** [**position**](/css/properties/position) or layout to use this property.

Element layout is set by providing a value for the [**height**](/css/properties/height) property or the [**width**](/css/properties/width) property.

## Related specifications

[CSS basic box model](http://www.w3.org/TR/css3-box/)
:   W3C Working Draft

[CSS 2.1, 8 Box model](http://www.w3.org/TR/CSS21/box.html#propdef-padding)
:   W3C Recommendation
