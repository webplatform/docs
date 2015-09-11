---
title: max-height
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5070850'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'All elements but non-replaced inline elements, table columns, and column groups'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'The percentage as specified or the absolute length or ''none'''
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`max-height`'
  Percentages: 'Of the height of containing block. If the height of the containing block depends on the content & the element does not have position as absolute, then this value becomes ''none''.'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Sets the maximum height for an element. It prevents the height of the element to exceed the specified value. If min-height is specified and is greater than max-height, max-height is overridden.'
tags:
  - CSS
  - Properties
uri: css/properties/max-height

---
## <span>Summary</span>

Sets the maximum height for an element. It prevents the height of the element to exceed the specified value. If min-height is specified and is greater than max-height, max-height is overridden.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `none`

Applies to
:   All elements but non-replaced inline elements, table columns, and column groups

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   The percentage as specified or the absolute length or 'none'

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `max-height`

Percentages
:   Of the height of containing block. If the height of the containing block depends on the content & the element does not have position as absolute, then this value becomes 'none'.

## <span>Syntax</span>

-   `max-height: calc()`
-   `max-height: fill-available`
-   `max-height: fit-content`
-   `max-height: inherit`
-   `max-height: length`
-   `max-height: max-content`
-   `max-height: min-content`
-   `max-height: none`
-   `max-height: percentage`

## <span>Values</span>

length
:   Specifies a fixed height. Negative values are not allowed. See [length](/css/data_types/length) for possible units.

percentage
:   A \<percentage\> relative to the height of the containing block. If the containing block has no height explicitly set then is is treated as none. Negative values are not allowed.

calc()
:   See [css calc function](/css/functions/calc) for mode details.

inherit
:   Takes the same specified value as the property for the element's parent.

none
:   Default. Clears the max-height value. The height property can have any value.

max-content
:   The narrowest space a box could take while fitting around its contents if none of the soft wrap opportunities within the box were taken.(Space/Punctuation in text are examples of a soft-wrap opportunity). Requires CSS Intrinsic & Extrinsic Sizing Module support in browsers.

min-content
:   The narrowest measure a box could take that doesn't lead to inline-dimension overflow that could be avoided by choosing a larger measure. Roughly, the measure that would fit around its contents if all soft wrap opportunities within the box were taken. Requires CSS Intrinsic & Extrinsic Sizing Module support in browsers.

fill-available
:   Fill the entire available space of from the containing block (Height minus horizontal margin, border and padding of the containing block). Requires CSS Intrinsic & Extrinsic Sizing Module support in browsers.

fit-content
:   If the total available space is finite, equals to min(max-content, max(min-content, fill-available)). Otherwise, equal to the max-content measure. Requires CSS Intrinsic & Extrinsic Sizing Module support in browsers.

## <span>Examples</span>

Use max-height with any CSS selector to apply it.

``` css
/* Restrict all div elements to a max-height of 10px */
div { max-height: 10px }
```

max-height property overrides the height of an element.

``` html
<style>
/*Default width. Height is based on the content*/
.without-max-height, .with-max-height {
    width: 100px;
}
/*Max height overrides height*/
.with-max-height {
    background: cyan;
    max-height: 50px;
}
.without-max-height {
    background: red;
}
</style>
<div class="without-max-height">Without Max Height. Height taken from content</div>
<br />
<div class="with-max-height">With Max Height. Content may overflow if it goes beyond height.</div>
<br />
<p><strong>Other elements</strong> will flow overtop of objects that are overflowed from their max-height containers.</p>
```

[View live example](http://code.webplatform.org/gist/5070850)

## <span>Usage</span>

     CSS max height is well supported across most browsers. A few things to consider while usage:

-   Both max-height & height should not be specified in the same units as one would override the other. The end result would be min(height, max-height).
-   [min-height](/css/properties/min-height) overrides max-height. If min-height supplied is greater than max-height, max-height does not have an impact.
-   max-content, min-content, fit-content, and fill-available are in W3C draft stage and not supported across all browsers.
-   Support for [calc](/css/functions/calc) is better across browsers. Vendor prefixes may be needed.

## <span>Related specifications</span>

[CSS 2.1 (Section 10.7)](http://www.w3.org/TR/CSS2/visudet.html#min-max-heights)
:   W3C Recommendation

[CSS Intrinsic & Extrinsic Sizing Module Level 3](http://dev.w3.org/csswg/css3-sizing/#width-height-keywords)
:   Working Draft

## <span>See also</span>

### <span>Related articles</span>

#### <span>Box Model</span>

-   [border](/css/properties/border)

-   [border-corner-shape](/css/properties/border-corner-shape)

-   [bottom](/css/properties/bottom)

-   [box-shadow](/css/properties/box-shadow)

-   [box-sizing](/css/properties/box-sizing)

-   [break-before](/css/properties/break-before)

-   [clear](/css/properties/clear)

-   [float](/css/properties/float)

-   [height](/css/properties/height)

-   [left](/css/properties/left)

-   [line-height](/css/properties/line-height)

-   [margin](/css/properties/margin)

-   [margin-bottom](/css/properties/margin-bottom)

-   [margin-left](/css/properties/margin-left)

-   [margin-right](/css/properties/margin-right)

-   [margin-top](/css/properties/margin-top)

-   **max-height**

-   [max-width](/css/properties/max-width)

-   [min-height](/css/properties/min-height)

-   [min-width](/css/properties/min-width)

### <span>External resources</span>

-   [W3C Wiki](http://www.w3.org/wiki/CSS/Properties/max-height)
-   [Internet Explorer Docs](http://msdn.microsoft.com/en-in/library/ie/ms530809(v=vs.85).aspx)
-   [Firefox Docs](https://developer.mozilla.org/en-US/docs/CSS/max-height)
-   [Safari Docs](https://developer.apple.com/library/safari/#documentation/AppleApplications/Reference/SafariCSSRef/Articles/StandardCSSProperties.html#//apple_ref/css/property/max-height)
-   [Can I Use](http://caniuse.com/#feat=minmaxwh)
