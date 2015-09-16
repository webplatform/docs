---
title: 'align-self'
code_samples:
  - 'http://gist.github.com/4745364'
compatibility:
  feature: align-self
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'flex items'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': '**auto** computes to parent''s **align-items**, or **stretch** if the element has no parent; otherwise as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`alignSelf`'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Allows the default alignment to be overridden for individual flex items.'
tags:
  - CSS
  - Properties
  - Flexbox
uri: css/properties/align-self

---
## Summary

Allows the default alignment to be overridden for individual flex items.

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
:   **auto** computes to parent's **align-items**, or **stretch** if the element has no parent; otherwise as specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `alignSelf`

## Syntax

-   `align-self: auto`
-   `align-self: baseline`
-   `align-self: center`
-   `align-self: flex-end`
-   `align-self: flext-start`
-   `align-self: stretch`
-   `flex-item-align: auto`
-   `flex-item-align: baseline`
-   `flex-item-align: center`
-   `flex-item-align: end`
-   `flex-item-align: start`
-   `flex-item-align: stretch`

## Values

auto
:   Computes to the value of [align-items](/css/properties/align-items) on the element's parent, or **stretch** if the element has no parent.

flext-start
:   The cross-start margin edge of the flex item is placed flush with the cross-start edge of the line.

flex-end
:   The cross-end margin edge of the flex item is placed flush with the cross-end edge of the line.

center
:   The flex item's margin box is centered in the cross axis within the line. (If the cross size of the flex line is less than that of the flex item, it will overflow equally in both directions.)

baseline
:   If the flex item's inline axis is the same as the cross axis, this value is identical to **flex-start**.

Otherwise, it participates in baseline alignment: all participating flex items on the line are aligned such that their baselines align, and the item with the largest distance between its baseline and its cross-start margin edge is placed flush against the cross-start edge of the line.

stretch
:   If the cross size property of the flex item is **auto**, its used value is the length necessary to make the cross size of the item's margin box as close to the same size as the line as possible, while still respecting the constraints imposed by [min-height](/css/properties/min-height)/[min-width](/css/properties/min-width)/[max-height](/css/properties/max-height)/[max-width](/css/properties/max-width). Note: that if the flex container's height is constrained the stretch value may cause the contents of the flex item to overflow the item.

## Examples

Displaying children with custom alignment.

``` css
.list {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.list div {
  flex: 1;
}

.list .second {
  align-self: flex-end;
}
```

[View live example](http://code.webplatform.org/gist/4745364)

## Notes

-   This property will have no effect if the flex-item's cross axis margins are set to auto.
-   This property was named **flex-item-align** in older drafts.

## Related specifications

[CSS Flexible Box Layout Module](http://www.w3.org/TR/css3-flexbox/#align-self-property)
:   Candidate Recommendation

## See also

### Related articles

#### CSS Layout

-   [Responsive Web Design](/concepts/mobile_web/responsive_design)

-   [@import](/css/atrules/@import)

-   **align-self**

-   [background](/css/properties/background)

-   [box-decoration-break](/css/properties/box-decoration-break)

-   [box-flex](/css/properties/box-flex)

-   [box-lines](/css/properties/box-lines)

-   [box-orient](/css/properties/box-orient)

-   [box-pack](/css/properties/box-pack)

-   [box-shadow](/css/properties/box-shadow)

-   [break-before](/css/properties/break-before)

-   [flex-align](/css/properties/flex-align)

-   [flex-item-align](/css/properties/flex-item-align)

-   [flex-line-pack](/css/properties/flex-line-pack)

-   [grid-auto-rows](/css/properties/grid-auto-rows)

-   [grid-definition-columns](/css/properties/grid-definition-columns)

-   [grid-definition-rows](/css/properties/grid-definition-rows)

-   [height](/css/properties/height)

-   [max-width](/css/properties/max-width)

-   [user-modify](/css/properties/user-modify)

-   [baseline-shift](/svg/attributes/baseline-shift)

#### Flexbox

-   [align-content](/css/properties/align-content)

-   [align-items](/css/properties/align-items)

-   **align-self**

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
