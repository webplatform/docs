---
title: flex-basis
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'flex items'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`flexBasis`'
  Percentages: 'relative to the main size of the flex container'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The flex-basis CSS property describes the initial main size of the flex item before any free space is distributed according to the flex factors described in the flex property (flex-grow and flex-shrink).'
tags:
  - CSS
  - Properties
  - Flexbox
uri: css/properties/flex-basis

---
## Summary

The flex-basis CSS property describes the initial main size of the flex item before any free space is distributed according to the flex factors described in the flex property (flex-grow and flex-shrink).

## Overview table

[Initial value](/css/concepts/initial_value)
:   `auto`

Applies to
:   flex items

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `flexBasis`

Percentages
:   relative to the main size of the flex container

## Syntax

-   `flex-basis: auto`
-   `flex-basis: height`
-   `flex-basis: width`

## Values

auto
:   The flex item's initial main size is determined by either the [width](/css/properties/width) or [height](/css/properties/height) property, whichever is in the main dimension, as determined by the [flex-direction](/css/properties/flex-flow) property. Note that the value of the [width](/css/properties/width) or [height](/css/properties/height) property itself may be **auto**, in which case the size is determined by the flex item's contents.

width
:   In a horizontal writing mode; percentage values of **flex-basis** are resolved against the flex item's flex container, and if that containing block's size is indefinite, the result is undefined.

height
:   In a vertical writing mode; percentage values of **flex-basis** are resolved against the flex item's flex container, and if that containing block's size is indefinite, the result is undefined.

## Examples

See [flex examples](/css/properties/flex#Examples) for the use of this property in an example.

``` css
flex-basis: 60%;
```

## Usage

     The best practice is to use (instead of this property) the flex shorthand property, as it correctly resets any unspecified flex components to accomodate common uses.

## Related specifications

[CSS Flexible Box Layout Model](http://dev.w3.org/csswg/css-flexbox/#flex-basis)
:   Candidate Recommendation

## See also

### Related articles

#### Flexbox

-   [align-content](/css/properties/align-content)

-   [align-items](/css/properties/align-items)

-   [align-self](/css/properties/align-self)

-   [break-before](/css/properties/break-before)

-   [flex](/css/properties/flex)

-   **flex-basis**

-   [flex-direction](/css/properties/flex-direction)

-   [flex-flow](/css/properties/flex-flow)

-   [flex-grow](/css/properties/flex-grow)

-   [flex-shrink](/css/properties/flex-shrink)

-   [flex-wrap](/css/properties/flex-wrap)

-   [justify-content](/css/properties/justify-content)
