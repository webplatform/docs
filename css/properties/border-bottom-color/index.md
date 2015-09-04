---
title: border-bottom-color
tags:
  - CSS
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
notes:
  - 'This article could be shortened. The various ways of color encoding needn''t be included in the example, as they are not specific to border-bottom-color. The link to the color article is sufficient.'
summary: "Sets the color of the bottom border. This page explains the border-bottom-color value, but often you will find it more convenient to fix the border's bottom color as part of a shorthand set, either border-bottom or border-color.\n"
code_samples:
  - 'http://gist.github.com/5535432'
uri: css/properties/border-bottom-color

---
# border-bottom-color

## Summary

Sets the color of the bottom border. This page explains the border-bottom-color value, but often you will find it more convenient to fix the border's bottom color as part of a shorthand set, either border-bottom or border-color.

[Colors](/css/data_types/color) can be defined several ways. For more information, see [Usage](/css/properties/border-bottom-color#Usage).

## Overview table

[Initial value](/css/concepts/initial_value)
:   `color - The value of the 'color' property`
Applies to
:   All elements
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   when taken from the 'color' property, the computed value of 'color'; otherwise, as specified
Animatable
:   Yes
[CSS Object Model Property](/css/concepts/cssom)
:   `borderTopColor`
Percentages
:   N/A

## Syntax

-   `border-bottom-color: <color>`
-   `border-bottom-color: currentColor`
-   `border-bottom-color: inherit`
-   `border-bottom-color: transparent`

## Values

\<color\>
:   The computed value of the ‘color’ property. This value can be a basic color keyword, such as red or lavenderblush, a numerical value, an RGB or RGBA value, or an HSL or HSLA value. For more information, see [Usage](/css/properties/border-bottom-color#Usage).

inherit
:   currentColor, the color value inherited from parent object.

currentColor
:   The same as ‘color: inherit’, the color value inherited from parent object.

transparent
:   Fully transparent. This keyword can be considered a shorthand for transparent black, rgba(0,0,0,0), which is its computed value.

## Examples

The following example demonstrates the use of `border-bottom-color` by creating a set of 7 boxes with the rainbow colors, each box using a different way of color code representation. (Some style rules omitted for brevity.)

``` {.css}
.box {
  border: 5px solid #efefef;
}

.named-value {
  border-bottom-color: red;
}

.hex-value {
  border-bottom-color: #FD6C02;
}

.rgb-value {
  border-bottom-color: rgb(255, 255, 0);
}

.rgb-percentage-value {
  border-bottom-color: rgb(0%, 100%, 0%);
}

.hsl-value {
  border-bottom-color: hsl(240, 100%, 50%);
}

.rgba-value {
  border-bottom-color: rgba(75, 0, 130, 0.8);
}

.hsla-value {
  border-bottom-color: hsla(282, 100%, 41%, 0.8);
}
```

[View live example](http://code.webplatform.org/gist/5535432)

``` {.html}
<div class="box named-value">
  <h1>Named color</h1>
  <p><code>red</code></p>
</div>

<div class="box hex-value">
  <h1>Hexadecimal color</h1>
  <p><code>#FD6C02</code></p>
</div>

<div class="box rgb-value">
  <h1>RGB color</h1>
  <p><code>rgb(255, 255, 0)</code></p>
</div>

<div class="box rgb-percentage-value">
  <h1>RGB percentage color</h1>
  <p><code>rgb(0%, 100%, 0%)</code></p>
</div>

<div class="box hsl-value">
  <h1>HSL color</h1>
  <p><code>hsl(240, 100%, 50%)</code></p>
</div>

<div class="box rgba-value">
  <h1>RGB with alpha color</h1>
  <p><code>rgba(75, 0, 130, 0.8)</code></p>
</div>

<div class="box hsla-value">
  <h1>HSL with alpha color</h1>
  <p><code>hsla(282, 100%, 41%, 0.8)</code></p>
</div>
```

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

-   **border-bottom-color**

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

### Related pages (MSDN)

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `defaultsSelected`
-   `runtimeStyle`
-   `style`
-   `border`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

