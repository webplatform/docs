---
title: 'border-top-color'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5535354'
compatibility:
  feature: border-top-color
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`color - The value of the ''color'' property`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'when taken from the ''color'' property, the computed value of ''color''; otherwise, as specified'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`borderTopColor`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: "Sets the color of an element's top border. This page explains the border-top-color value, but often you will find it more convenient to fix the border's top color as part of a shorthand set, either border-top or border-color.\n"
tags:
  - CSS
  - Properties
uri: css/properties/border-top-color

---
## Summary

Sets the color of an element's top border. This page explains the border-top-color value, but often you will find it more convenient to fix the border's top color as part of a shorthand set, either border-top or border-color.

[Colors](/css/data_types/color) can be defined several ways. For more information, see [Usage](/css/properties/border-top-color#Usage).

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

-   `border-top-color: <color>`
-   `border-top-color: currentColor`
-   `border-top-color: inherit`
-   `border-top-color: transparent`

## Values

\<color\>
:   The computed value of the ‘color’ property. This value can be a basic color keyword, such as red or lavenderblush, a numerical value, an RGB or RGBA value, or an HSL or HSLA value. For more information, see [Usage](/css/properties/border-top-color#Usage).

inherit
:   currentColor, the color value inherited from parent object.

currentColor
:   The same as ‘color: inherit’, the color value inherited from parent object.

transparent
:   Fully transparent. This keyword can be considered a shorthand for transparent black, rgba(0,0,0,0), which is its computed value.

## Examples

The following example demonstrates the use of `border-top-color` by creating a set of 7 boxes with the rainbow colors, each box using a different way of color code representation. (Some style rules omitted for brevity.)

``` css
.box {
  border: 5px solid #efefef;
}

.named-value {
  border-top-color: red;
}

.hex-value {
  border-top-color: #FD6C02;
}

.rgb-value {
  border-top-color: rgb(255, 255, 0);
}

.rgb-percentage-value {
  border-top-color: rgb(0%, 100%, 0%);
}

.hsl-value {
  border-top-color: hsl(240, 100%, 50%);
}

.rgba-value {
  border-top-color: rgba(75, 0, 130, 0.8);
}

.hsla-value {
  border-top-color: hsla(282, 100%, 41%, 0.8);
}
```

[View live example](http://code.webplatform.org/gist/5535354)

``` html
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

-   **border-top-color**

-   [border-top-left-radius](/css/properties/border-top-left-radius)

-   [border-top-right-radius](/css/properties/border-top-right-radius)

-   [border-top-style](/css/properties/border-top-style)

-   [border-top-width](/css/properties/border-top-width)

-   [border-width](/css/properties/border-width)

-   border-top[border-top](/css/properties/border-top)
-   border-color[border-color](/css/properties/border-color)
-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   defaultsSelected[defaultsSelected](/dom/HTMLOptionElement/defaultSelected)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
-   border[border](/css/properties/border)
