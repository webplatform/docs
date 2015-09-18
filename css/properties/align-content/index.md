---
title: 'align-content'
code_samples:
  - 'http://code.webplatform.org/gist/5536244'
compatibility:
  feature: align-content
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`stretch`'
  'Applies to': 'multi-line flex containers'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`alignContent`'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Aligns a flex container''s lines within the flex container when there is extra space in the cross-axis, similar to how justify-content aligns individual items within the main-axis.'
tags:
  - CSS_Properties
  - CSS
  - Flexbox
uri: css/properties/align-content

---
## Summary

Aligns a flex container's lines within the flex container when there is extra space in the cross-axis, similar to how justify-content aligns individual items within the main-axis.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `stretch`

Applies to
:   multi-line flex containers

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   specified value

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `alignContent`

## Syntax

-   `align-content: center`
-   `align-content: flex-end`
-   `align-content: flex-start`
-   `align-content: space-around`
-   `align-content: space-between`
-   `align-content: stretch`
-   `flex-line-pack: center`
-   `flex-line-pack: distribute`
-   `flex-line-pack: end`
-   `flex-line-pack: justify`
-   `flex-line-pack: start`
-   `flex-line-pack: stretch`

## Values

flex-start
:   Lines are packed toward the start of the flex container. The cross-start edge of the first line in the flex container is placed flush with the cross-start edge of the flex container, and each subsequent line is placed flush with the preceding line.

flex-end
:   Lines are packed toward the end of the flex container. The cross-end edge of the last line is placed flush with the cross-end edge of the flex container, and each preceding line is placed flush with the subsequent line.

center
:   Lines are packed toward the center of the flex container. The lines in the flex container are placed flush with each other and aligned in the center of the flex container, with equal amounts of empty space between the cross-start content edge of the flex container and the first line in the flex container, and between the cross-end content edge of the flex container and the last line in the flex container. (If the leftover free-space is negative, the lines will overflow equally in both directions.)

space-between
:   Lines are evenly distributed in the flex container. If the leftover free-space is negative this value is identical to **flex-start**. Otherwise, the cross-start edge of the first line in the flex container is placed flush with the cross-start content edge of the flex container, the cross-end edge of the last line in the flex container is placed flush with the cross-end content edge of the flex container, and the remaining lines in the flex container are distributed so that the empty space between any two adjacent lines is the same.

space-around
:   Lines are evenly distributed in the flex container, with half-size spaces on either end. If the leftover free-space is negative this value is identical to **center**. Otherwise, the lines in the flex container are distributed such that the empty space between any two adjacent lines is the same, and the empty space before the first and after the last lines in the flex container are half the size of the other empty spaces.

stretch
:   Lines stretch to take up the remaining space. If the leftover free-space is negative, this value is identical to **flex-start**. Otherwise, the free-space is split equally between all of the lines, increasing their cross size.

## Examples

Spacing lines within a multi-line flex container. Change the values in the live example.

``` css
.container {
    display:         flex;
    flex-flow: row wrap;
    align-content: space-around;
    width: 400px;
    height: 200px;
    background: #CCC;
}

.container div {
    height: 30px;   /* set this to 'auto' to see how the lines respond to 'align-items: stretch' */
    margin: 0px;
}

.container .third-item {
  width: 160px;
  background: #CC3333;
  font-size: 14px;
}

.container .second-item {
  width: 140px;
  background: #FFFC33;
}

.container .first-item {
  width: 100px;
  background: #3333FF;
}
```

[View live example](http://code.webplatform.org/gist/5536244)

## Notes

-   This property has no effect when the flexbox has only a single line. Only flex containers with multiple lines can ever have free space in the cross-axis for lines to be aligned in, because in a flex container with a single line the sole line automatically stretches to fill the space.
-   This property was named **flex-line-pack** in earlier drafts.

## Related specifications

[CSS Flexible Box Layout Module](http://www.w3.org/TR/css3-flexbox/#align-content-property)
:   Candidate Recommendation

## See also

### Related articles

#### Flexbox

-   **align-content**

-   [align-items](/css/properties/align-items)

-   [align-self](/css/properties/align-self)

-   [break-before](/css/properties/break-before)

-   [flex](/css/properties/flex)

-   [flex-basis](/css/properties/flex-basis)

-   [flex-direction](/css/properties/flex-direction)

-   [flex-flow](/css/properties/flex-flow)

-   [flex-grow](/css/properties/flex-grow)

-   [flex-shrink](/css/properties/flex-shrink)

-   [flex-wrap](/css/properties/flex-wrap)

-   [justify-content](/css/properties/justify-content)

### External resources

Also, check out the following live demo sites:

-   [Flexbox Playground](http://demo.agektmr.com/flexbox/)
-   [Flexy Boxes](http://the-echoplex.net/flexyboxes)
