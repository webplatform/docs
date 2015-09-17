---
title: 'background'
code_samples:
  - 'http://gist.github.com/6114809'
  - 'http://gist.github.com/6115439'
compatibility:
  feature: background
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`[[Initial value::see individual properties: * background-color * background-position * background-size * background-repeat * background-attachment * background-clip * background-origin * background-image]]`'
  'Applies to': 'all elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'see individual properties'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`background`'
  Percentages: 'see individual properties'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: "This background property is a shorthand property for setting the color, position, size, repeat, clip, origin, attachment, and image of the element.\n"
tags:
  - CSS_Properties
uri: css/properties/background

---
## Summary

This background property is a shorthand property for setting the color, position, size, repeat, clip, origin, attachment, and image of the element.

The background- properties provide fundamental styles to an element, such as color, image, and position. CSS3 adds more properties for handling backgrounds, including properties that improve the mobile web experience. Many CSS background properties can be set, at the same time, with this background property.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `[[Initial value::see individual properties: * background-color * background-position * background-size * background-repeat * background-attachment * background-clip * background-origin * background-image]]`

Applies to
:   all elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   see individual properties

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `background`

Percentages
:   see individual properties

## Syntax

-   `background: <attachment>`
-   `background: <bg-image>`
-   `background: <box>{1,2}`
-   `background: <color>`
-   `background: <position> [ / <bg-size> ]?`
-   `background: <repeat-style>`

## Values

\<bg-image\>
:   Any of the values available to [**background-image**](/css/properties/background-image) property. The default value is `none`.

\<position\> [ / \<bg-size\> ]?
:   Any of the values available to [**background-position**](/css/properties/background-position) property. Otherwise, it is set to its initial value.

\<repeat-style\>
:   Any of the values available to [**background-repeat**](/css/properties/background-repeat) property. The default value is `repeat`.

\<attachment\>
:   Any of the values available to [**background-attachment**](/css/properties/background-attachment) property. The default value is `scroll`.

\<box\>{1,2}
:   If one \<box\> value is present then it sets both [**background-origin**](/css/properties/background-origin) and [**background-clip**](/css/properties/background-clip) to that value. If two values are present, then the first sets [**background-origin**](/css/properties/background-origin) and the second [**background-clip**](/css/properties/background-clip).

For background-clip, valid values are those available to [**background-clip**](/css/properties/background-clip) property. The default value is `border-box`. For background-origin, valid values are those available to [**background-origin**](/css/properties/background-origin) property. The default value is `padding-box`.

\<color\>
:   Any of the values available to [**background-color**](/css/properties/background-color) property. The default value is `transparent`.

## Examples

The background property is set to the color \#f06 on the p element.

``` css
p {
    background: #f06;
}
```

[View live example](http://gist.github.com/6114809)

Only one background property is set on the body. Many individual properties have been specified for the p element, including a background image that only shows up on the p element.

``` css
body {
    background: #90ee90;
    font-family: 'Bitter';

}
p { background: url(http://www.webplatform.org/logo/wplogo_transparent_xlg.png)
                40% / 20em
                #ffffe0
                round
                fixed
                border-box;
}
```

[View live example](http://gist.github.com/6115439)

## Usage

     The background property is a shorthand property that can set almost all of the background- properties. The specification has examples of how to use the shorthand property and what that usage translates to.

## Notes

The background of the root element becomes the background of the canvas and extends to cover the entire canvas, but only for that element alone. For an example, see [[1]](http://gist.github.com/6115439).

## Related specifications

[CSS Level 3](http://www.w3.org/TR/css3-background/)
:   Candidate Recommendation

[CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS21/colors.html#propdef-background)
:   Recommendation

## See also

### Related articles

#### CSS Layout

-   [Responsive Web Design](/concepts/mobile_web/responsive_design)

-   [@import](/css/atrules/@import)

-   [align-self](/css/properties/align-self)

-   **background**

-   [box-decoration-break](/css/properties/box-decoration-break)

-   [box-flex](/css/properties/box-flex)

-   [box-lines](/css/properties/box-lines)

-   [box-orient](/css/properties/box-orient)

-   [box-pack](/css/properties/box-pack)

-   [box-shadow](/css/properties/box-shadow)

-   [break-before](/css/properties/break-before)

-   [flex-align](/css/properties/flex-align)

-   [flex-item-align](/css/properties/flex-item-align)

-   [flex-line-pack](/css/properties/flex-line-pack)

-   [grid-auto-rows](/css/properties/grid-auto-rows)

-   [grid-definition-columns](/css/properties/grid-definition-columns)

-   [grid-definition-rows](/css/properties/grid-definition-rows)

-   [height](/css/properties/height)

-   [max-width](/css/properties/max-width)

-   [user-modify](/css/properties/user-modify)

-   [baseline-shift](/svg/attributes/baseline-shift)

#### Background

-   [background](/css/cssom/properties/background)

-   **background**

-   [background-attachment](/css/properties/background-attachment)

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [background-clip](/css/properties/background-clip)

-   [background-color](/css/properties/background-color)

-   [background-image](/css/properties/background-image)

-   [background-origin](/css/properties/background-origin)

-   [background-position](/css/properties/background-position)

-   [background-position-x](/css/properties/background-position-x)

-   [background-position-y](/css/properties/background-position-y)

-   [background-repeat](/css/properties/background-repeat)

-   [background-size](/css/properties/background-size)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### Other articles

-   [Using Multiple Backgrounds](/tutorials/using_css_multiple_background)
-   [CSS\_background\_images](/tutorials/CSS_background_images)

### External resources

-   [Backgrounds In CSS: Everything You Need To Know](http://coding.smashingmagazine.com/2009/09/02/backgrounds-in-css-everything-you-need-to-know/), By Michael Martin
-   [CSS Background shorthand coming to mobile WebKit browsers](http://updates.html5rocks.com/2013/02/CSS-Background-shorthand-coming-to-mobile-WebKit-browsers), By Stephen Thomas
-   [Simple Responsive Images With CSS Background Images](http://mobile.smashingmagazine.com/2013/07/22/simple-responsive-images-with-css-backgrounds/), By Stephen Thomas
-   [Just One of Those Weird Things About CSS: Background on body](http://css-tricks.com/just-one-of-those-weird-things-about-css-background-on-body/), By Chris Coyier
-   [background](http://css-tricks.com/almanac/properties/b/background/), By Chris Coyier
