---
title: 'border'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/).'
code_samples:
  - 'http://gist.github.com/5534182'
compatibility:
  feature: border
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`medium none currentColor`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'concatenation of `border-width`, `border-style`, and `border-color`.'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`border`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Shorthand property that defines the different properties of all four sides of an element''s border in a single declaration. It can be used to set border-width, border-style and border-color, or a subset of these.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/border

---
## Summary

Shorthand property that defines the different properties of all four sides of an element's border in a single declaration. It can be used to set border-width, border-style and border-color, or a subset of these.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `medium none currentColor`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   concatenation of `border-width`, `border-style`, and `border-color`.

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `border`

Percentages
:   N/A

## Syntax

-   `border: <border-width> OR <border-style> OR <border-color>`
-   `border: inherit`

## Values

inherit
:   When the value is set to `inherit`, the element will inherit the border values set on its parent.

\<border-width\> OR \<border-style\> OR \<border-color\>
:   A concatenation of `<border-width>`, `<border-style>`, and `<border-color>`. At least one of these must be present, and they may appear in any order.

**\<border-width\>**: A numeric value with any of the standard length units. The initial value is `medium`, which most browsers will render as 3px. See the [border-width](/css/properties/border-width) property.

**\<border-style\>**: This takes any of the range of values available to the [border-style](/css/properties/border-style) property. The initial value is `none`.

**\<border-color\>**: This takes any valid CSS color. See the [border-color](/css/properties/border-color) property. The initial value is `currentColor`.

## Examples

A simple example showing multiple `<div>`s, identical in style except that they have different `border` properties applied to them.

``` html
<div class="one"><p>One</p></div>
<div class="two"><p>Two</p></div>
<div class="three"><p>Three</p></div>
<div class="four"><p>Four</p></div>
<div class="five"><p>Five</p></div>
```

[View live example](http://gist.github.com/5534182)

``` css
/**
 * border example
**/

div {
  width: 150px;
  height: 150px;
  margin: 1rem;
  float: left;
}

p {
  padding: 2rem;
}

.one {
  /* The most basic border example you can show. */
  border: 1px solid black;
}

.two {
  /* If you don't explicitly set a color, currentColor is used, which
     equates to the text colour of the element, in this case black.   */
  border: 4px dashed;
}

.three {
  /* When no width is specified, the default width medium is used,
     which computes to about 3px in most browsers */
  border: dotted red;
}

.four {
  /* When no border style is specified, the border won't appear,
     as the default border style is none. */
  border: 10px black;
}

.five {
  /* A more interesting border example to round things off. */
  border: 10px inset rgba(234,190,50,0.75);
}
```

[View live example](http://gist.github.com/5534182)

## Usage

     * It is usual to first use the border shorthand property to set the state of a default box, and then override it where needed, using the more specific shorthand properties border-width, border-style, and border-color. Each of these properties may take up to four values, respective to the sides of the box.

-   It is also common to override the `border` property with the properties specific to each individual side: `border-top`, `border-right`, `border-bottom`, and `border-left`. Each of these properties may take up to three values, defining the appearance (width, style, and color) of the designated side.
-   The following twelve "longhand" properties can be used to define the entire border of an object:

`border-top-width`, `border-top-style`, `border-top-color`, `border-right-width`, `border-right-style`, `border-right-color`, `border-bottom-width`, `border-bottom-style`, `border-bottom-color`, `border-left-width`, `border-left-style`, `border-left-color`.

## Notes

-   The initial value of `border` is the concatenated result of the initial values of each component.
-   A `border-bottom` can be used as a divider between vertically laid out items, such as navigation menu items, or a new section. Authors will sometimes use this technique rather than inserting an `<hr/>` element in the HTML.
-   Another common technique is to use `border-bottom` properties for link underlining rather than `text-decoration: underline`, as it affords the designer more control.

## Related specifications

[CSS Level 3](http://www.w3.org/TR/css3-background/#borders)
:   Candidate Recommendation

[CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/box.html#border-shorthand-properties)
:   Recommendation

[CSS Level 1](http://www.w3.org/TR/CSS1/#border)
:   Recommendation

## See also

### Related articles

#### Border

-   **border**

-   [border-bottom](/css/properties/border-bottom)

-   [border-bottom-color](/css/properties/border-bottom-color)

-   [border-bottom-left-radius](/css/properties/border-bottom-left-radius)

-   [border-bottom-style](/css/properties/border-bottom-style)

-   [border-bottom-width](/css/properties/border-bottom-width)

-   [border-color](/css/properties/border-color)

-   [border-image](/css/properties/border-image)

-   [border-image-outset](/css/properties/border-image-outset)

-   [border-image-repeat](/css/properties/border-image-repeat)

-   [border-image-slice](/css/properties/border-image-slice)

-   [border-image-source](/css/properties/border-image-source)

-   [border-image-width](/css/properties/border-image-width)

-   [border-left](/css/properties/border-left)

-   [border-left-color](/css/properties/border-left-color)

-   [border-left-style](/css/properties/border-left-style)

-   [border-left-width](/css/properties/border-left-width)

-   [border-radius](/css/properties/border-radius)

-   [border-right](/css/properties/border-right)

-   [border-right-color](/css/properties/border-right-color)

-   [border-right-style](/css/properties/border-right-style)

-   [border-right-width](/css/properties/border-right-width)

-   [border-top](/css/properties/border-top)

-   [border-top-color](/css/properties/border-top-color)

-   [border-top-left-radius](/css/properties/border-top-left-radius)

-   [border-top-right-radius](/css/properties/border-top-right-radius)

-   [border-top-style](/css/properties/border-top-style)

-   [border-top-width](/css/properties/border-top-width)

-   [border-width](/css/properties/border-width)

#### Box Model

-   **border**

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

-   [min-width](/css/properties/min-width)

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   defaultSelected[defaultSelected](/dom/HTMLOptionElement/defaultSelected)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
