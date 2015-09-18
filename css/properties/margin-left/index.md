---
title: 'margin-left'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://code.webplatform.org/gist/5727939'
compatibility:
  feature: margin-left
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`Depends on the particular element. Different elements have different default margins.`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified, but with relative lengths converted into absolute pixel values.'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`marginLeft`'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'margin-left sets the left margin of an element.'
tags:
  - CSS_Properties
  - CSS
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected
uri: css/properties/margin-left

---
## Summary

margin-left sets the left margin of an element.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `Depends on the particular element. Different elements have different default margins.`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified, but with relative lengths converted into absolute pixel values.

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `marginLeft`

## Syntax

-   `margin-left: auto`
-   `margin-left: inherit`
-   `margin-left: length`
-   `margin-left: percentage`

## Values

length
:   Specifies a fixed length, using any standard [CSS length units](/css/units/length) . Negative Values are allowed.

percentage
:   A percentage of the width of the containing block. Negative values are allowed. (Even though this is margin-top, the browser will take the percentage from the width, not the height of the containing block.)

auto
:   The browser calculates a left margin dependent on the space available.

inherit
:   Inherits the parent element's specified `margin-left` width.

## Examples

In this example there are three blocks, styled identically except for their `margin-left` values:

-   The first one has a `margin-left` of 2 centimeters, meaning that it is pushed over to the right by 2cm.
-   The second one has no `margin-left` of its own, to indicate the default position of the blocks.
-   The bottom block has a `margin-left` of -10% set on it, meaning that it is pushed over to the left by 10% of the parent element's width.

``` html
<div class="one"></div>
<div class="two"></div>
<div class="three"></div>
```

[View live example](http://code.webplatform.org/gist/5727939)

CSS applied to the HTML shown in the first example.

``` css
/**
 * margin-left examples
 **/

 * {
   margin: 0;
 }

 div {
   width: 200px;
   height: 100px;
   background: linear-gradient(rgba(0,0,0,0.25), rgba(0,0,0,0));
   border-radius: 10px;
 }

 .one {
   background-color: red;
   margin-left: 2cm;
 }

 .two {
   background-color: blue;
 }

 .three {
   background-color: green;
   margin-left: -10%;
 }
```

[View live example](http://code.webplatform.org/gist/5727939)

## Usage

     ===Usage===

-   When calculating the height and width of an element, DO NOT include the margins in your calculations (i.e. include everything else: content area, padding, and border). However, DO include margin size when calculating available space within an element's containing element.
-   When two margins collide, for example when one block level element has a right margin set, and a floated element directly to the right of it has a left margin set, the larger of the two margins remains, and the smaller one collapses and disappears.
-   Margins are always transparent.

### Best Practices

-   When possible, use [margin](/css/properties/margin) shorthand (i.e. {margin: 10px 15px 20px 15px;}) to specify margin-widths rather than writing out each margin's specifications as this clutters code and makes it difficult to read. Use `margin-bottom` if there is a specific reason to call attention to it (e.g. one element has a different bottom margin than the rest in its class, etc.).

## Notes

You can specify possible length values relative to the height of the element's font (`em`) or the height of the letter "x" (`ex`). In Microsoft Internet Explorer 3.0, the specified margin value is added to the default value of the object. In Microsoft Internet Explorer 4.0 and later, the margin value is absolute. The margin properties do not work with the **td** and **tr** objects in Internet Explorer 4.0, but they do work in Internet Explorer 3.0. To set margins in the cell for Internet Explorer 4.0 and later, apply the margin to an object, such as **div** or **p**, within the **td**. This property applies to inline elements, starting with Microsoft Internet Explorer 5.5. With earlier versions of Windows Internet Explorer, inline elements must have an **absolute** [**position**](/css/properties/position) or layout to use this property. Element layout is set by providing a value for the [**height**](/css/properties/height) property or the [**width**](/css/properties/width) property. Negative margins are supported, except for top and bottom margins on inline objects.

### Standards Information

[w3.org](http://www.w3.org/TR/CSS2/box.html#propdef-margin-left)

## Related specifications

[CSS 2](http://www.w3.org/TR/CSS2/box.html#propdef-margin-left)
:   W3C Recommendation

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

-   **margin-left**

-   [margin-right](/css/properties/margin-right)

-   [margin-top](/css/properties/margin-top)

-   [max-height](/css/properties/max-height)

-   [max-width](/css/properties/max-width)

-   [min-height](/css/properties/min-height)

-   [min-width](/css/properties/min-width)

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   defaults[defaults](/w/index.php?title=dom/defaultSelected&action=edit&redlink=1)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
