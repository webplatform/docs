---
title: 'outline-color'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/Web/CSS/outline-color)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5566688'
compatibility:
  feature: outline-color
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`invert`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'The computed value for ‘invert’ is ‘invert’. For \<color\> values, the computed value is as defined for the ‘color’ property.'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`outlineColor`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The outline-color property sets the color of the outline of an element. An outline is a line that is drawn around elements, outside the border edge, to make the element stand out.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/outline-color

---
## Summary

The outline-color property sets the color of the outline of an element. An outline is a line that is drawn around elements, outside the border edge, to make the element stand out.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `invert`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   The computed value for ‘invert’ is ‘invert’. For \<color\> values, the computed value is as defined for the ‘color’ property.

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `outlineColor`

Percentages
:   N/A

## Syntax

-   `outline-color: <color>`
-   `outline-color: inherit`
-   `outline-color: invert`

## Values

\<color\>
:   Specify the color to use on all outlines. This can be anywhere from one to four values representing the top, right, bottom, and left outline respectively.

invert
:   This is expected to perform a color inversion on the pixels on the screen.

inherit
:   This is a keyword indicating that the value is inherited from their parent's element calculated value.

## Examples

An example of using outline color

``` html
<div class="outline">I ♥ WebPlatform.org!</div>
<div class="outline outline--blue">I ♥ WebPlatform.org!</div>
<div class="outline outline--green">I ♥ WebPlatform.org!</div>
<div class="outline outline--invert">I ♥ WebPlatform.org!</div>
```

[View live example](http://gist.github.com/5566688)

Multiple classes that change the original outline color

``` css
/*
  outline color example
*/

.outline--green {
  /* make the outline green */
  outline-color: #00ff00;
}

.outline--blue {
  /* make the outline blue */
  outline-color: #0000ff;
}

.outline--invert {
    /* outline invert */
    outline-color: invert;
}
```

[View live example](http://gist.github.com/5566688)

## Usage

     The color value can be a numerical value, such as one of the following:

-   a basic color keyword, such as "red"
-   a hex value, such as \#ff0000
-   an red-green-blue (RGB) value, such as rgb(255,0,0)
-   an RGB-alpha (RGBA) that includes color opacity, such as rgba(255,0,0,1) or rgba(100%,0%,0%,1)
-   a hue-saturation-lightness (HSL), such as hsl(0, 100%, 50%)
-   HSLa, such as hsl(0, 100%, 50%, 1)

The color value can also be an extended keyword, such as aliceblue or lavenderblush. For a full list of extended keywords, see the [CSS Color Module Level 3 spec](http://www.w3.org/TR/css3-color/#svg-color), which is the consolidation of various specifications.

## Notes

-   A value of **invert** ensures that the outline is visible regardless of the background color.
-   The [outline](/css/properties/outline) property is a shorthand property for setting one or more of the individual outline properties [outline-style](/css/properties/outline-style), [outline-width](/css/properties/outline-width) and **outline-color** in a single rule. In most cases the use of this shortcut is preferable and more convenient.

## Related specifications

[CSS Basic User Interface Module Level 3 (CSS3 UI)](http://dev.w3.org/csswg/css-ui/#outline-color)
:   Working Draft
