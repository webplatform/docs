---
title: border-color
tags:
  - CSS
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: "The CSS border-color property sets the color of an element's four borders. This property can have from one to four values, made up of the elementary properties: \n"
code_samples:
  - 'http://gist.github.com/5546053'
uri: css/properties/border-color

---
# border-color

## Summary

The CSS border-color property sets the color of an element's four borders. This property can have from one to four values, made up of the elementary properties:

-   [border-top-color](/css/properties/border-top-color)
-   [border-right-color](/css/properties/border-right-color)
-   [border-bottom-color](/css/properties/border-bottom-color)
-   [border-left-color](/css/properties/border-left-color)

The default color is the currentColor of each of these values.

If you provide one value, it sets the color for the element. Two values set the horizontal and vertical values, respectively. Providing three values sets the top, vertical, and bottom values, in that order. Four values set all for sides: top, right, bottom, and left, in that order.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `color: The value of the 'color' property for each of the border sides border-top-color, border-right-color, border-bottom-color, and border-left-color.`
Applies to
:   All elements
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   See individual properties
Animatable
:   Yes
[CSS Object Model Property](/css/concepts/cssom)
:   `borderColor`
Percentages
:   N/A

## Syntax

-   `border-color: <color>`
-   `border-color: currentColor`
-   `border-color: inherit`
-   `border-color: transparent`

## Values

\<color\>
:   Specify the color to use on all borders. This can be anywhere from one to four values representing the top, right, bottom, and left border respectively.

inherit
:   Is a keyword indicating that all four values are inherited from their parent's element calculated value.

transparent
:   This will apply a border that is not visible but it can have a width applied.

currentColor
:   The same as ‘color: inherit’, the color value inherited from parent object.

## Examples

A simple example showing how to use the border-color property on HTML div elements.

``` {.css}
.one {
          color: #6CC644;
          border: medium solid;
        }

        /* You can use other color on each side */
        .two {
          border: 10px solid;
          border-color: #6CC644 #FFC621 #DE6525 #256A84;
        }

        /* You can use other color for other styles */
        .three {
          border-width: 5px;
          border-style: ridge dashed solid;
          border-color: #6CC644 #DE6525;
        }

        /* You can set horizontal and vertical using just two color values (horizontal is first then vertical) */
        .four {
            border-width: 3px;
            border-style: solid;
            border-color: #ccc #666;
        }
```

[View live example](http://code.webplatform.org/gist/5546053)

## Usage

     The color value can be a property keyword, an extended keyword, or a numerical value. The two property keywords are currentColor and transparent. currentColor is the ‘color’ property value from the parent object. transparent is shorthand for transparent black, rgba(0,0,0,0).

The color value can also be a numerical value, such as one of the following:

-   a basic color keyword, such as "red"
-   a hex value, such as \#ff0000
-   an red-green-blue (RGB) value, such as rgb(255,0,0)
-   an RGB-alpha (RGBA) that includes color opacity, such as rgba(255,0,0,1) or rgba(100%,0%,0%,1)
-   a hue-saturation-lightness (HSL), such as hsl(0, 100%, 50%)
-   HSLa, such as hsl(0, 100%, 50%, 1)

The color value can also be an extended keyword, such as aliceblue or lavenderblush. For a full list of extended keywords, see the [CSS Color Module Level 3 spec](http://www.w3.org/TR/css3-color/#svg-color), which is the consolidation of various specifications.

## Related specifications

Specification
:   Status
[CSS Level 3 - Backgrounds and Borders Module](http://www.w3.org/TR/css3-background/#the-border-color)
:   W3C Candidate Recommendation
[CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/box.html#border-color-properties)
:   W3C Recommendation
[CSS Level 3 - Color Module](http://www.w3.org/TR/css3-color)
:   W3C Recommendation

## See also

### Related articles

#### Border

-   [border](/css/properties/border)

-   [border-bottom](/css/properties/border-bottom)

-   [border-bottom-color](/css/properties/border-bottom-color)

-   [border-bottom-left-radius](/css/properties/border-bottom-left-radius)

-   [border-bottom-style](/css/properties/border-bottom-style)

-   [border-bottom-width](/css/properties/border-bottom-width)

-   **border-color**

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

### Related pages

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `defaultsSelected`
-   `runtimeStyle`
-   `style`
-   `border`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/border-color)

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

