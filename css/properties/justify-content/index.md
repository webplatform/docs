---
title: 'justify-content'
code_samples:
  - 'http://gist.github.com/5842739'
compatibility:
  feature: justify-content
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`flex-start`'
  'Applies to': 'flex containers'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The justify-content property aligns flex items along the main axis of the current line of the flex container, similarly to how align-items aligns items in the cross axis.'
tags:
  0: CSS
  1: Properties
  3: Flexbox
uri: css/properties/justify-content

---
## Summary

The justify-content property aligns flex items along the main axis of the current line of the flex container, similarly to how align-items aligns items in the cross axis.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `flex-start`

Applies to
:   flex containers

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   specified value

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

## Syntax

-   `-ms-flex-pack: center`
-   `-ms-flex-pack: end`
-   `-ms-flex-pack: justify`
-   `-ms-flex-pack: start`
-   `justify-content: center`
-   `justify-content: flex-end`
-   `justify-content: flex-start`
-   `justify-content: space-around`
-   `justify-content: space-between`

## Values

flex-start
:   Flex items are packed toward the start of the line. The main-start margin edge of the first flex item on the line is placed flush with the main-start edge of the line, and each subsequent flex item is placed flush with the preceding item.

flex-end
:   Flex items are packed toward the end of the line. The main-end margin edge of the last flex item is placed flush with the main-end edge of the line, and each preceding flex item is placed flush with the subsequent item.

center
:   Flex items are packed toward the center of the line. The flex items on the line are placed flush with each other and aligned in the center of the line, with equal amounts of empty space between the main-start edge of the line and the first item on the line and between the main-end edge of the line and the last item on the line. (If the leftover free-space is negative, the flex items will overflow equally in both directions.)

space-between
:   Flex items are evenly distributed in the line. If the leftover free-space is negative or there is only a single flex item on the line, this value is identical to ‘flex-start’. Otherwise, the main-start margin edge of the first flex item on the line is placed flush with the main-start edge of the line, the main-end margin edge of the last flex item on the line is placed flush with the main-end edge of the line, and the remaining flex items on the line are distributed so that the spacing between any two adjacent items is the same.

space-around
:   Flex items are evenly distributed in the line, with half-size spaces on either end. If the leftover free-space is negative or there is only a single flex item on the line, this value is identical to ‘center’. Otherwise, the flex items on the line are distributed such that the spacing between any two adjacent flex items on the line is the same, and the spacing between the first/last flex items and the flex container edges is half the size of the spacing between flex items.

## Examples

An example with the justify-content property, demonstrating the different options.

``` css
.container {
  display: flex;

  width: 800px;
  height: 100px;
  background: #CCC;
}

.container div {
  flex: 0;

  height: 100px;
  margin: 0px;
  font-family: Bitter;
  font-size: 24px;
}

.third-item {
  width: 150px;
  background: #CC3333;

}

.second-item {
  width: 275px;
  background: #FFFC33;
}

.first-item {
  width: 200px;
  background: #3333FF;
}

.flex-start {
  justify-content: flex-start;
}

.flex-end {
  justify-content: flex-end;
}

.justifycenter {
  justify-content: center;
}

.space-around {
  justify-content: space-around;
}

.space-between {
  justify-content: space-between;
}
```

[View live example](http://code.webplatform.org/gist/5842739)

``` html
<p>justify-content: flex-start</p>
<div class="container flex-start">
  <div class="first-item">first-item</div>
  <div class="second-item">second-item</div>
  <div class="third-item">third-item</div>
</div>
<p>justify-content: flex-end</p>
<div class="container flex-end">
  <div class="first-item">first-item</div>
  <div class="second-item">second-item</div>
  <div class="third-item">third-item</div>
</div>
<p>justify-content: center</p>
<div class="container justifycenter">
  <div class="first-item">first-item</div>
  <div class="second-item">second-item</div>
  <div class="third-item">third-item</div>
</div>
<p>justify-content: space-around</p>
<div class="container space-around">
  <div class="first-item">first-item</div>
  <div class="second-item">second-item</div>
  <div class="third-item">third-item</div>
</div>
<p>justify-content: space-between</p>
<div class="container space-between">
  <div class="first-item">first-item</div>
  <div class="second-item">second-item</div>
  <div class="third-item">third-item</div>
</div>
```

## Notes

This property was named **flex-pack** in earlier drafts.

## Related specifications

[CSS Flexible Box Layout Module](http://dev.w3.org/csswg/css-flexbox/#justify-content-property)
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

-   [flex-shrink](/css/properties/flex-shrink)

-   [flex-wrap](/css/properties/flex-wrap)

-   **justify-content**

### External resources

Also, check out the following live demo sites:

-   [Flexbox Playground](http://demo.agektmr.com/flexbox/)
-   [Flexy Boxes](http://the-echoplex.net/flexyboxes)
