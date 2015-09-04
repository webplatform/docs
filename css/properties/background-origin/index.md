---
title: background-origin
tags:
  - CSS
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Specifies what the background-position property is relative to.'
uri: css/properties/background-origin

---
# background-origin

## Summary

Specifies what the background-position property is relative to.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `padding-box`
Applies to
:   All elements
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   as specified
Animatable
:   No
[CSS Object Model Property](/css/concepts/cssom)
:   `backgroundOrigin`
Percentages
:   N/A

## Syntax

-   `background-origin: border-box`
-   `background-origin: content-box`
-   `background-origin: padding-box`

## Values

padding-box
:   Default. The position is relative to the padding box.

border-box
:   The position is relative to the border box.

content-box
:   The position is relative to the content box. Useful for having background images automatically follow the padding.

## Examples

``` {.html}
<style>
/**
 * Background-origin Example
 */
.border-box {
  background-origin: border-box;
}
.content-box {
  background-origin: content-box;
}
.padding-box {
  background-origin: padding-box;
}
div {
  display: inline-block;
  margin: 10px;
  width: 100px;
  height: 60px;
  background-color: hsl(0,50%,90%);
  padding: 20px;
  border: 10px solid black;
  background-origin: border-box;
  background-image: url("http://docs.webplatform.org/w/skins/webplatform/images/logo.svg");
  background-repeat: no-repeat;
}
</style>

<div class="border-box">Border box!</div>
<div class="padding-box">Padding box!</div>
<div class="content-box">Content box!</div>
```

[[live example](http://code.webplatform.org/gist/5842945) View live example]

## Usage

     You should understand the CSS Box Model before using this property.  Use this in conjunction with background-image and optionally background-position.   See background position for information about the coordinate system and positioning.

## Notes

### Remarks

For elements rendered as a single box, the **background-origin** property specifies the background positioning area. For elements rendered as multiple boxes (for instance, inline boxes on several lines or boxes on several pages), this property specifies which boxes determine the background positioning areas. If the [**background-attachment**](/css/properties/background-attachment) value for this image is **fixed**, then the **background-origin** property has no effect. In this case, the background positioning area is the initial containing block. In Windows Internet Explorer 9, the background of a box can have multiple layers. The number of layers is determined by the number of comma-separated values in the [**background-image**](/css/properties/background-image) property. Each of the images is sized, positioned, and tiled according to the corresponding value in the other background properties ([**background-attachment**](/css/properties/background-attachment), [**background-clip**](/css/properties/background-clip), **background-origin**, [**background-position**](/css/properties/background-position), [**background-repeat**](/css/properties/background-repeat), and [**background-size**](/css/properties/background-size)). The first image in the list is the layer closest to the user, the next one is painted behind the first, and so on.

## Related specifications

Specification
:   Status
[CSS Backgrounds & Borders Level 3](http://www.w3.org/TR/css3-background/#the-background-origin)
:   W3C Candidate Recommendation

## See also

### Related articles

#### Background

-   [background](/css/cssom/properties/background)

-   [background](/css/properties/background)

-   [background-attachment](/css/properties/background-attachment)

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [background-clip](/css/properties/background-clip)

-   [background-color](/css/properties/background-color)

-   [background-image](/css/properties/background-image)

-   **background-origin**

-   [background-position](/css/properties/background-position)

-   [background-position-x](/css/properties/background-position-x)

-   [background-position-y](/css/properties/background-position-y)

-   [background-repeat](/css/properties/background-repeat)

-   [background-size](/css/properties/background-size)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/background-origin)

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

