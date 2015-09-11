---
title: flex-grow
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`0`'
  'Applies to': 'flex items'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`flexGrow`'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The flex-grow CSS property specifies how much a flex item will enlarge with respect to the other items in the flex container to fill an expanded container.'
tags:
  - CSS
  - Properties
  - Flexbox
uri: css/properties/flex-grow

---
## <span>Summary</span>

The flex-grow CSS property specifies how much a flex item will enlarge with respect to the other items in the flex container to fill an expanded container.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `0`

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
:   `flexGrow`

## <span>Syntax</span>

-   `flex-grow: number`

## <span>Values</span>

number
:   The flex grow factor, which describes the proportion by which the flex item will grow relative to the other flex items in the container. Negative numbers are invalid.

## <span>Examples</span>

See [flex examples](/css/properties/flex#Examples) for the use of this property in an example.

``` css
flex-grow: 3;
```

## <span>Usage</span>

     The best practice is to use (instead of this property) the flex shorthand property, as it correctly resets any unspecified flex components to accomodate common uses.

## <span>Notes</span>

This property is animatable only for values of 1 or greater.

## <span>Related specifications</span>

[CSS Flexible Box Layout Model](http://dev.w3.org/csswg/css-flexbox/#flex-grow)
:   Candidate Recommendation

## <span>See also</span>

### <span>Related articles</span>

#### <span>Flexbox</span>

-   [align-content](/css/properties/align-content)

-   [align-items](/css/properties/align-items)

-   [align-self](/css/properties/align-self)

-   [break-before](/css/properties/break-before)

-   [flex](/css/properties/flex)

-   [flex-basis](/css/properties/flex-basis)

-   [flex-direction](/css/properties/flex-direction)

-   [flex-flow](/css/properties/flex-flow)

-   **flex-grow**

-   [flex-shrink](/css/properties/flex-shrink)

-   [flex-wrap](/css/properties/flex-wrap)

-   [justify-content](/css/properties/justify-content)
