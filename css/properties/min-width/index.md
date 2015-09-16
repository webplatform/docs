---
title: min-width
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5842171'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`0`'
  'Applies to': 'all elements but non-replaced inline elements, tables, inline tables, table cells, table columns, and column groups'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'the percentage as specified or the absolute length or ''none'''
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`min-width`'
  Percentages: 'yes'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Sets the minimum width of an element. It limits the width property to be not smaller than the value specified in min-width.'
tags:
  - CSS
  - Properties
uri: css/properties/min-width

---
## Summary

Sets the minimum width of an element. It limits the width property to be not smaller than the value specified in min-width.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `0`

Applies to
:   all elements but non-replaced inline elements, tables, inline tables, table cells, table columns, and column groups

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   the percentage as specified or the absolute length or 'none'

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `min-width`

Percentages
:   yes

## Syntax

-   `min-width: calc()`
-   `min-width: fill-available`
-   `min-width: fit-content`
-   `min-width: inherit`
-   `min-width: length`
-   `min-width: max-content`
-   `min-width: min-content`
-   `min-width: none`
-   `min-width: percentage`

## Values

length
:   Specifies a fixed width. Negative values are not allowed. See [length](/css/data_types/length) for possible units.

percentage
:   A \<percentage\> relative to the width of the containing block. If the containing block has no width explicitly set then is is treated as none. Negative values are not allowed.

calc()
:   See [css calc function](/css/functions/calc) for mode details.

inherit
:   Takes the same specified value as the property for the element's parent.

none
:   Default. Clears the min-width value. The width property can have any value.

max-content
:   The narrowest space a box could take while fitting around its contents if none of the soft wrap opportunities within the box were taken.(Space/Punctuation in text are examples of a soft-wrap opportunity). Requires CSS Intrinsic & Extrinsic Sizing Module support in browsers.

min-content
:   The narrowest measure a box could take that doesn't lead to inline-dimension overflow that could be avoided by choosing a larger measure. Roughly, the measure that would fit around its contents if all soft wrap opportunities within the box were taken. Requires CSS Intrinsic & Extrinsic Sizing Module support in browsers.

fill-available
:   Fill the entire available space of from the containing block (Width minus vertical margin, border and padding of the containing block). Requires CSS Intrinsic & Extrinsic Sizing Module support in browsers.

fit-content
:   If the total available space is finite, equals to min(max-content, max(min-content, fill-available)). Otherwise, equal to the max-content measure. Requires CSS Intrinsic & Extrinsic Sizing Module support in browsers.

## Examples

Use min-width with any CSS selector to apply it.

``` html
/* Restrict all div elements to a min-width of 100px */
div { min-width: 100px }
```

Constrain the width of a **div** element using **min-width** and [**max-width**](/css/properties/max-width) attributes.

``` html
<style>
/* Width set to 50% */
.width {
    width:50%;
    background:#eee;
}

/* min-width set to 600px */
.minwidth {
    width: 50%;
    min-width: 600px;
    background: lightblue;
}

/* max-width set to 600px */
.maxwidth {
    width: 50%;
    max-width: 200px;
    background: lightgreen
}

/* Content with border and padding */
.content {
    border:1px solid #c00;
    padding:5px;
}
</style>

<h3>Resize the window to grow and shrink the div from max to min width.</h3>
<div class="width">
        <p class="content">This div also has a width of 50%. <br/><br/>
         Note that the div height increases to accommodate the flow of text.</p>
</div>
<div class="minwidth">
    <p class="content">This div also has a width of 50%.<br /><br /> It also has a min-width of 600px.</p>
</div>
<div class="maxwidth">
    <p class="content">This div also has a width of 50%.<br /><br /> It also has a max-width of 200px.</p>
</div>
```

[View live example](http://code.webplatform.org/gist/5842171)

## Usage

     CSS min width is well supported across most browsers. A few things to consider while usage:

-   min-width overrides [max-width](/css/properties/max-width). If min-width supplied is greater than max-width, max-width does not have an impact.
-   max-content, min-content, fit-content, and fill-available are in W3C draft stage and not supported across all browsers.
-   Support for [calc](/css/functions/calc) is better across browsers. Vendor prefixes may be needed.

## Notes

### Remarks

The **min-width**/[**max-width**](/css/properties/max-width) attributes apply to floating and absolutely positioned block and inline-block elements, as well as some intrinsic controls. They do not apply to non-replaced inline elements, such as table rows and row/column groups. (A "replaced" element has intrinsic dimensions, such as an **img** or **textArea**.) This property is enabled only under the strict [!DOCTYPE](/html/elements/!DOCTYPE).

## Related specifications

[CSS 2.1 (Section 10.4)](http://www.w3.org/TR/CSS2/visudet.html#min-max-widths)
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

-   [min-height](/css/properties/min-height)

-   **min-width**

### Related pages (MSDN)

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `runtimeStyle`
-   `style`
-   `Cascading Style Sheet Compatibility in Internet Explorer 7`
