---
title: align-items
code_samples:
  - 'http://gist.github.com/5533982'
  - 'http://gist.github.com/4745348'
  - 'http://gist.github.com/4745341'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`stretch`'
  'Applies to': 'flex containers'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`alignItems`'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Sets the default alignment in the cross axis for all of the flex container''s items, including anonymous flex items, similarly to how justify-content aligns items along the main axis.'
tags:
  - CSS
  - Properties
uri: css/properties/align-items

---
## <span>Summary</span>

Sets the default alignment in the cross axis for all of the flex container's items, including anonymous flex items, similarly to how justify-content aligns items along the main axis.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `stretch`

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
:   `alignItems`

## <span>Syntax</span>

-   `align-items: baseline`
-   `align-items: center`
-   `align-items: flex-end`
-   `align-items: flex-start`
-   `align-items: stretch`
-   `box-align: after`
-   `box-align: baseline`
-   `box-align: before`
-   `box-align: middle`
-   `box-align: stretch`
-   `flex-align: baseline`
-   `flex-align: center`
-   `flex-align: end`
-   `flex-align: start`
-   `flex-align: stretch`

## <span>Values</span>

flex-start
:   The cross-start margin edge of the flex item is placed flush with the cross-start edge of the line.

flex-end
:   The cross-end margin edge of the flex item is placed flush with the cross-end edge of the line.

center
:   The flex item's margin box is centered in the cross axis within the line. (If the cross size of the flex line is less than that of the flex item, it will overflow equally in both directions.)

baseline
:   If the flex item's inline axis is the same as the cross axis, this value is identical to 'flex-start'. Otherwise, it participates in baseline alignment: all participating flex items on the line are aligned such that their baselines align, and the item with the largest distance between its baseline and its cross-start margin edge is placed flush against the cross-start edge of the line.

stretch
:   If the cross size property of the flex item is **auto**, its used value is the length necessary to make the cross size of the item's margin box as close to the same size as the line as possible, while still respecting the constraints imposed by [min-height](/css/properties/min-height)/[min-width](/css/properties/min-width)/[max-height](/css/properties/max-height)/[max-width](/css/properties/max-width). Note: that if the flex container's height is constrained the **stretch** value may cause the contents of the flex item to overflow the item.

## <span>Examples</span>

Alignment of flex items in a flex container. Change the values in the live example.

``` css
.container {
  display: flex;

  width: 400px;
  height: 200px;
  background: #CCC;

  align-items: center; /* values: flex-start, flex-end, center, baseline, stretch */
}

.container div {
  flex: 1;

  width: 100px;
  height: auto;        /* let this be set to see how the items respond to 'align-items: stretch' */
  margin: 0px;
  font-family: Bitter;
  font-size: 24px;
}

.container .third-item {
  height: 110px;         /* disable this to see how the item responds to 'align-items: stretch' */
  background: #CC3333;
  font-size: 14px;       /* over-loading the font size so this item will respond to 'align-items: baseline' */
}

.container .second-item {
  height: 140px;         /* disable this to see how the item responds to 'align-items: stretch' */
  background: #FFFC33;
}

.container .first-item {
  height: 160px;        /* disable this to see how the item responds to 'align-items: stretch' */
  background: #3333FF;
}
```

[View live example](http://code.webplatform.org/gist/5533982)

Displaying children centered horizontally.

``` css
.list {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.list div {
  flex: 1;
}
```

[View live example](http://code.webplatform.org/gist/4745348)

Displaying children centered vertically.

``` css
.list {
  display: flex;
  flex-direction: row;
  align-items: center;
  height: 100px;
}

.list div {
  flex: 1;
}
```

[View live example](http://code.webplatform.org/gist/4745341)

## <span>Notes</span>

This property was named **flex-align** in older drafts.

## <span>Related specifications</span>

[CSS Flexible Box Layout Module](http://www.w3.org/TR/css3-flexbox/#align-items-property)
:   Candidate Recommendation

## <span>See also</span>

### <span>Related articles</span>

#### <span>Flexbox</span>

-   [align-content](/css/properties/align-content)

-   **align-items**

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

### <span>External resources</span>

Also, check out the following live demo sites:

-   [Flexbox Playground](http://demo.agektmr.com/flexbox/)
-   [Flexy Boxes](http://the-echoplex.net/flexyboxes)
