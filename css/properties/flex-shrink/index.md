---
title: flex-shrink
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`1`'
  'Applies to': 'flex items'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`flexShrink`'
readiness: 'Ready to Use'
summary: 'The flex-shrink CSS property specifies how much a flex item will be reduced with respect to the other items in the flex container to fit within a reduced container.'
tags:
  - CSS
  - Properties
  - Flexbox
uri: css/properties/flex-shrink

---
## Summary

The flex-shrink CSS property specifies how much a flex item will be reduced with respect to the other items in the flex container to fit within a reduced container.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `1`

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
:   `flexShrink`

## Syntax

-   `flex-shrink: number`

## Values

number
:   The flex shrink factor, which describes the proportion by which the flex item will shrink relative to the other flex items in the container. Negative numbers are invalid.

## Examples

See [flex examples](/css/properties/flex#Examples) for the use of this property in an example.

``` css
flex-shrink: 3;
```

## Usage

     The best practice is to use (instead of this property) the flex shorthand property, as it correctly resets any unspecified flex components to accomodate common uses.

## Notes

This property is animatable only for values of 1 or greater.

## Related specifications

[CSS Flexible Box Layout Model](http://dev.w3.org/csswg/css-flexbox/#flex-shrink)
:   Candidate Recommendation

## See also

### Related articles

#### Flexbox

-   [align-content](/css/properties/align-content)

-   [align-items](/css/properties/align-items)

-   [align-self](/css/properties/align-self)

-   [break-before](/css/properties/break-before)

-   [flex](/css/properties/flex)

-   [flex-basis](/css/properties/flex-basis)

-   [flex-direction](/css/properties/flex-direction)

-   [flex-flow](/css/properties/flex-flow)

-   [flex-grow](/css/properties/flex-grow)

-   **flex-shrink**

-   [flex-wrap](/css/properties/flex-wrap)

-   [justify-content](/css/properties/justify-content)
