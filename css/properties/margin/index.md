---
title: 'margin'
code_samples:
  0: 'http://code.webplatform.org/gist/5727296'
  2: 'http://code.webplatform.org/gist/5727295'
compatibility:
  feature: margin
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`Depends on the particular element. Different elements have different default margins.`'
  'Applies to': 'All elements except elements with table display types other than table-caption, table, and inline-table'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified, but with relative lengths converted into absolute pixel values.'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`margin`'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The margin property is shorthand to allow you to set all four margins of an element at once. Its equivalent longhand properties are margin-top, margin-right, margin-bottom and margin-left. Negative values are also allowed.'
tags:
  - CSS_Properties
  - CSS
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected
uri: css/properties/margin

---
## Summary

The margin property is shorthand to allow you to set all four margins of an element at once. Its equivalent longhand properties are margin-top, margin-right, margin-bottom and margin-left. Negative values are also allowed.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `Depends on the particular element. Different elements have different default margins.`

Applies to
:   All elements except elements with table display types other than table-caption, table, and inline-table

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified, but with relative lengths converted into absolute pixel values.

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `margin`

## Syntax

-   `margin: auto`
-   `margin: inherit`
-   `margin: length`
-   `margin: percentage`

## Values

length
:   Specifies a fixed length, using any standard [CSS length units](/css/units/length) . Negative Values are allowed.

percentage
:   A percentage relative to the width of the containing block. Negative values are allowed.

auto
:   `auto` is replaced by some suitable value by the browser. For example, it can be used for centering of blocks.

`div { width:50%;  margin:0 auto; }` centers the `<div>` container horizontally.

inherit
:   Causes the element it is applied to to take on the same margin values as its parent.

## Examples

A simple example showing different combinations of margin values applied to three identically sized elements.

-   The first one has a margin of 50 pixels on all sides.
-   The second one has no margin on the top and bottom, but `auto` set on the left and right, causing it to center in the parent container.
-   The third one has four individual values, including a negative top margin, causing it to move up, above the level of the second container, and a large left margin, causing it to be shunted over to the right.

``` html
<div class="one"></div>
<div class="two"></div>
<div class="three"></div>
```

[View live example](http://code.webplatform.org/gist/5727296)

The CSS applied to the above HTML.

``` css
/**
 * margin examples
 */

/**
  * It is strongly rocommended to NOT do this, if you want to
  *   have an even styling for all browsers you should have a
  *   look at current CSS reset technique.   In the case of this
  *   example, it is only to demonstrate cascading.
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
  margin: 50px
}

.two {
  background-color: blue;
  margin: 0px auto;
}

.three {
  background-color: green;
  margin: -11em 0px 0px 210px;
}
```

[View live example](http://code.webplatform.org/gist/5727296)

The following example demonstrates the different ways of using the `margin` property.

``` css
.text-margin {
  /*
  This uses the margin: value syntax.
  value can be specified in em, px etc.
  */
  margin: 1em;
}

.text-vertical-horizontal {
  /*
  This uses the margin: horizontal vertical syntax.
  horizontal is the amount of margin for both the side, left and side.
  Similarly, vertical is for both, top and bottom sides.
  */
  margin: 2rem 50px;
}

.text-top-horizontal-bottom {
  /*
  This uses the margin: top horizontal bottom syntax.
  */
  margin: 10pt 1em 1cm;
}

.text-top-right-bottom-left {
  /*
  This uses the margin: top right bottom left syntax.
  */
  margin: 5mm 1in 5ex 10ch;
}
```

[View live example](http://code.webplatform.org/gist/5727295)

The HTML accompanying the above example.

``` html
<div class="container">
  <p class="text-margin">This paragraph uses the <code>margin: value</code> syntax.</p>
</div>

<div class="container">
  <p class="text-vertical-horizontal">This paragraph uses the <code>margin: horizontal vertical</code> syntax.</p>
</div>

<div class="container">
  <p class="text-top-horizontal-bottom">This paragraph uses the <code>margin: top horizontal bottom</code> syntax.</p>
</div>

<div class="container">
  <p class="text-top-right-bottom-left">This paragraph uses the <code>margin: top right bottom left</code> syntax.</p>
</div>
```

## Usage

     * margin can take 1-4 values for its value, including CSS length units, percentage values, or the keywords auto or inherit:

-   -   If one value is given, it applies to all four sides.
    -   If two values are given, the first applies to the top and bottom, the second applies to the right and left.
    -   If three values are given, the first applies to the top, the second applies to the right and left sides, and the third applies to the bottom.
    -   If four values are given, they are applied in clockwise order, starting from the top (top, right, bottom, left).
-   Negative margins are supported except for top and bottom margins on inline objects.
-   When two margins collide, for example when one block level element has a bottom margin set, immediately followed by another block level element with a top margin, the larger of the two margins remains, and the smaller one collapses and disappears.
-   Margins are always transparent.

## Related specifications

[CSS 2.1 (Section 8.3)](http://www.w3.org/TR/CSS2/box.html#margin-properties)
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

-   **margin**

-   [margin-bottom](/css/properties/margin-bottom)

-   [margin-left](/css/properties/margin-left)

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
-   `Conceptual`
-   `CSS Values and Units Reference`
-   `Other Resources`
-   `CSS Enhancements in Internet Explorer 6`
