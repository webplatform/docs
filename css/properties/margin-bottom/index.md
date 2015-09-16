---
title: margin-bottom
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/ms530802(v=vs.85).aspx) Article]'
code_samples:
  - 'http://gist.github.com/5727822'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`Depends on the particular element. Different elements have different default margins.`'
  'Applies to': 'All elements except elements with table display types other than table-caption, table, and inline-table.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified, but with relative lengths converted into absolute pixel values.'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`marginBottom`'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'margin-bottom sets the bottom margin of an element.'
tags:
  - CSS
  - Properties
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected
uri: css/properties/margin-bottom

---
## Summary

margin-bottom sets the bottom margin of an element.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `Depends on the particular element. Different elements have different default margins.`

Applies to
:   All elements except elements with table display types other than table-caption, table, and inline-table.

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified, but with relative lengths converted into absolute pixel values.

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `marginBottom`

## Syntax

-   `margin-bottom: auto`
-   `margin-bottom: inherit`
-   `margin-bottom: length`
-   `margin-bottom: percentage`

## Values

length
:   Specifies a fixed length, using any standard [CSS length units](http://docs.webplatform.org/wiki/css/units/length) . Negative Values are allowed.

percentage
:   A percentage of the width of the containing block. Negative values are allowed. (Even though this is margin-bottom, the browser will take the percentage from the width, not the height of the containing block.)

auto
:   The browser calculates a bottom margin dependent on the space available

inherit
:   Inherits the parent element's specified `margin-bottom` width.

## Examples

In this example there are three blocks, styled identically except for their `margin-bottom` values:

-   The first one has a `margin-bottom` of 2 centimeters, meaning that everything else is pushed down by 2cm, leaving a gap between the top block and the rest of the content.
-   The second one has a `margin-bottom` of -1em, meaning that the bottom block is actually pulled upwards so it overlaps the second block slightly.
-   The bottom block has no `margin-bottom` of its own.

``` html
<div class="one"></div>
<div class="two"></div>
<div class="three"></div>
```

[View live example](http://code.webplatform.org/gist/5727822)

CSS applied to the HTML shown in the first example.

``` css
/**
 * margin-bottom examples
 */

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
  margin-bottom: 2cm;
}

.two {
  background-color: blue;
  margin-bottom: -1em;
}

.three {
  background-color: green;
  margin-bottom: 0px;
}
```

[View live example](http://code.webplatform.org/gist/5727822)

## Usage

     ===Usage===

-   When calculating the height and width of an element, DO NOT include the margins in your calculations (i.e. include everything else: content area, padding, and border). However, DO include margin size when calculating available space within an element's containing element.
-   When two margins collide, for example when one block level element has a bottom margin set, immediately followed by another block level element with a top margin, the larger of the two margins remains, and the smaller one collapses and disappears.
-   Margins are always transparent.

### Best Practices

-   When possible, use [margin](http://docs.webplatform.org/wiki/css/properties/margin) shorthand (i.e. {margin: 10px 15px 20px 15px;}) to specify margin-widths rather than writing out each margin's specifications as this clutters code and makes it difficult to read. Use `margin-bottom` if there is a specific reason to call attention to it (e.g. one element has a different bottom margin than the rest in its class, etc.).

## Notes

As of Microsoft Internet Explorer 4.0 or later, you can specify possible length values relative to the height of the element's font (`em`) or the height of the letter "x" (`ex`). In Microsoft Internet Explorer 3.0, the specified margin value is added to the default value of the object. In Internet Explorer 4.0 or later, the margin value is absolute. The margin properties do not work with the **td** and **tr** objects in Internet Explorer 4.0, but they do work in Internet Explorer 3.0. To set margins in the cell for Internet Explorer 4.0 or later, apply the margin to an object, such as **div** or **p**, within the **td**. As of Microsoft Internet Explorer 5.5, this property applies to inline elements. With earlier versions of Windows Internet Explorer, inline elements must have an **absolute** [**position**](/css/properties/position) or layout to use this property. Element layout is set by providing a value for the [**height**](/css/properties/height) property or the [**width**](/css/properties/width) property. For inline elements, the value of this property is used to compute the border area of a surrounding inline element, if present. This value does not contribute to the height of a line. Negative margins are supported, except for top and bottom margins on inline objects.

## Related specifications

[CSS 2](http://www.w3.org/TR/CSS2/box.html#propdef-margin-bottom)
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

-   **margin-bottom**

-   [margin-left](/css/properties/margin-left)

-   [margin-right](/css/properties/margin-right)

-   [margin-top](/css/properties/margin-top)

-   [max-height](/css/properties/max-height)

-   [max-width](/css/properties/max-width)

-   [min-height](/css/properties/min-height)

-   [min-width](/css/properties/min-width)

### Related pages (MSDN)

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `defaults`
-   `runtimeStyle`
-   `style`
