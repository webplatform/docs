---
title: 'box-sizing'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/box-sizing)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809) Article]'
code_samples:
  - 'http://gist.github.com/5496267'
compatibility:
  feature: box-sizing
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`content-box`'
  'Applies to': 'all elements that accept width or height'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The box-sizing property alters the CSS box model used to calculate widths and heights of elements, so that they can be equal to the width and height of the content-, padding- or border-box.'
tags:
  - CSS
  - Properties
uri: css/properties/box-sizing

---
## Summary

The box-sizing property alters the CSS box model used to calculate widths and heights of elements, so that they can be equal to the width and height of the content-, padding- or border-box.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `content-box`

Applies to
:   all elements that accept width or height

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   specified value

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:

## Syntax

-   `box-sizing: border-box`
-   `box-sizing: content-box`
-   `box-sizing: padding-box`

## Values

content-box
:   The `width` and `height` properties (also including `min-width`, `max-width`, `min-height` and `max-height` properties) are calculated as the width/height of the content, but not the border, margin, or padding. This is the traditional behaviour of width and height as specified by CSS2.1.

padding-box
:   The `width` and `height` (also including `min-width`, `max-width`, `min-height` and `max-height` properties) of an element are calculated as the width/height of the content plus the `padding`. The dimensions of the content alone are thus calculated by subtracting the padding widths from each side of the element. Dimension properties are set to 0 if the calculated value is less than 0.

border-box
:   The `width` and `height` (also including `min-width`, `max-width`, `min-height` and `max-height` properties) of an element are calculated as the width/height of the content plus the `padding` and `border`.

The dimensions of the content alone are thus calculated by subtracting the padding and border widths from each side of the element. Dimension properties are set to 0 if the calculated value is less than 0.

## Examples

The following examples assume markup that looks like this.

``` html
<div class="parent">
    <div class="child"></div>
</div>
```

This CSS makes it so that the child `<div>` will always An element with padding that occupies half the width of its parent. This works because it has `box-sizing: border-box` set on it, so the total width will always be content plus padding plus border. As the border and padding get thicker, the element doesn't get larger. Instead, the content gets smaller to make way for the change.

``` css
/* Support Firefox, WebKit, Opera and IE8+ */

.parent {
   width: 50%;
   height: 200px;
   background: red;
 }

 .child {
    border: 30px solid rgba(0,0,0,0.5);
    float: left;
    padding: 3rem;
    background: blue;
    width: 50%;
    height: 100px;
    box-sizing: border-box;
 }
```

[View live example](http://code.webplatform.org/gist/5496267)

Input elements with type `search` are rendered with `border-box` in Safari 5 and Chrome. You can normalize this behavior across all browsers using the following code.

``` css
input[type="search"] {
    box-sizing: content-box;
}
```

## Related specifications

[CSS Level 3 - Basic User Interface Module](http://www.w3.org/TR/css3-ui/#box-sizing)
:   W3C Working Draft

## See also

### Related articles

#### Box Model

-   [border](/css/properties/border)

-   [border-corner-shape](/css/properties/border-corner-shape)

-   [bottom](/css/properties/bottom)

-   [box-shadow](/css/properties/box-shadow)

-   **box-sizing**

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

### Other articles

-   [WebPlatform.org tutorial on Box Model](http://docs.webplatform.org/wiki/tutorials/box_model)

### External resources

-   A [detailed article on box-sizing](http://css-tricks.com/box-sizing/) by Chris Coyier.
-   Paul Irish wrote about [applying `box-sizing: border-box;` on all elements](http://paulirish.com/2012/box-sizing-border-box-ftw/).
