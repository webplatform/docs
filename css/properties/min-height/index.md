---
title: 'min-height'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5842440'
compatibility:
  feature: min-height
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto (0 for non-flex elements)`'
  'Applies to': 'All elements but non-replaced inline elements, table columns, and column groups'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'The percentage as specified or the absolute length'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`min-height`'
  Percentages: 'Of the height of containing block. If the height of the containing block depends on the content & the element does not have position as absolute, then this value becomes 0.'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: "Sets the minimum height for an element. It prevents the height of the element to exceed the specified value.\nIt overrides both the height &amp; the max-height property if any them is specified below the min-height value.\n"
tags:
  - CSS
  - Properties
uri: css/properties/min-height

---
## Summary

Sets the minimum height for an element. It prevents the height of the element to exceed the specified value. It overrides both the height &amp; the max-height property if any them is specified below the min-height value.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `auto (0 for non-flex elements)`

Applies to
:   All elements but non-replaced inline elements, table columns, and column groups

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   The percentage as specified or the absolute length

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `min-height`

Percentages
:   Of the height of containing block. If the height of the containing block depends on the content & the element does not have position as absolute, then this value becomes 0.

## Syntax

-   `min-height: auto`
-   `min-height: calc`
-   `min-height: fill-available`
-   `min-height: fit-content`
-   `min-height: inherit`
-   `min-height: length`
-   `min-height: max-content`
-   `min-height: min-content`
-   `min-height: percentage`

## Values

auto
:   Default. Behaves as 0 for non-flexbox elements. On [flexbox](/css/flexbox) acts as min-content.

length
:   Specifies a fixed height. Negative values are not allowed. See [length](/css/data_types/length) for possible units.

percentage
:   A \<percentage\> relative to the height of the containing block. If the containing block has no height explicitly set then is is treated as 0. Negative values are not allowed

calc
:   See [css calc function](/css/functions/calc) for mode details.

inherit
:   Takes the same specified value as the property for the element's parent.

max-content
:   The narrowest space a box could take while fitting around its contents if none of the soft wrap opportunities within the box were taken.(Space/Punctuation in text are examples of a soft-wrap opportunity). Requires CSS Intrinsic & Extrinsic Sizing Module support in browsers.

min-content
:   The narrowest measure a box could take that doesn't lead to inline-dimension overflow that could be avoided by choosing a larger measure. Roughly, the measure that would fit around its contents if all soft wrap opportunities within the box were taken. Requires CSS Intrinsic & Extrinsic Sizing Module support in browsers.

fill-available
:   Fill the entire available space of from the containing block (Height minus horizontal margin, border and padding of the containing block). Requires CSS Intrinsic & Extrinsic Sizing Module support in browsers.

fit-content
:   If the total available space is finite, equals to min(max-content, max(min-content, fill-available)). Otherwise, equal to the max-content measure. Requires CSS Intrinsic & Extrinsic Sizing Module support in browsers.

## Examples

Use min-height with any CSS selector to apply it.

``` css
/* Ensure all div elements are a min-height of 100px */
div { min-height: 100px }
```

min-height property overrides the height of an element.

``` html
<style>
/* min-height example */

/*Default width. Height is based on the content*/
.without-min-height, .with-min-height {
    width: 100px;
}

/*Max height overrides height*/
.with-min-height {
    background: cyan;
    min-height: 300px;
}

.without-min-height {
    background: red;
}

.content {
    border: 1px solid black;
    padding: 10px;
}
</style>

<div class="without-min-height"><p class="content">Without Min Height. Height taken from content (with black border).</p></div>
<br />
<div class="with-min-height"><p class="content">With Min Height. Content (with black border) may not fill entirety of element.</p></div>
```

[View live example](http://code.webplatform.org/gist/5842440)

## Usage

     CSS min height is well supported across most browsers. A few things to consider while usage:

-   min-height overrides [max-height](/css/properties/max-height). If min-height supplied is greater than max-height, max-height does not have an impact.
-   max-content, min-content, fit-content, and fill-available are in W3C draft stage and not supported across all browsers.
-   Support for [calc](/css/functions/calc) is better across browsers. Vendor prefixes may be needed.

## Related specifications

[CSS 2.1 (Section 10.7)](http://www.w3.org/TR/CSS2/visudet.html#min-max-heights)
:   W3C Recommendation

[CSS Intrinsic & Extrinsic Sizing Module Level 3](http://dev.w3.org/csswg/css3-sizing/#width-height-keywords)
:   Working Draft

## See also

### Related articles

#### Box Model

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

-   [max-height](/css/properties/max-height)

-   [max-width](/css/properties/max-width)

-   **min-height**

-   [min-width](/css/properties/min-width)

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
-   `Reference`
-   height[height](/html/attributes/height)
-   `Other Resources`
-   `Cascading Style Sheet Compatibility in Internet Explorer 7`
-   `CSS Enhancements in Internet Explorer 6`
