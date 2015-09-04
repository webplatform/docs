---
title: color
tags:
  - CSS
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The color property sets the color of an element''s foreground content (usually text), accepting any standard CSS color from keywords and hex values to RGB(a) and HSL(a).'
code_samples:
  - 'http://gist.github.com/5502992'
uri: css/properties/color
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - css/color/value

---
# color

## Summary

The color property sets the color of an element's foreground content (usually text), accepting any standard CSS color from keywords and hex values to RGB(a) and HSL(a).

## Overview table

[Initial value](/css/concepts/initial_value)
:   `black, except in a few cases (see notes)`
Applies to
:   All elements
[Inherited](/css/concepts/inherited)
:   Yes
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   For a non-translucent color, an hexadecimal equivalent is used. Otherwise it is the RGBa equivalent
Animatable
:   Yes
[CSS Object Model Property](/css/concepts/cssom)
:   `color`
Percentages
:   NA

## Syntax

-   `color: color`

## Values

color
:   [CSS color value](/css/color)

## Examples

``` {.css}
/* Setting a paragraph color to turquoise with a name value */
p {color:turquoise}

/* Setting the same propriety with an hexadecimal value*/
p {color:#40E0D0}

/* with a RGB decimal value */
p { color: rgb(64,224,208) }

/* with a RGB percentage value */
p { color: rgb(25.1%,87.8%,81.6%) }

/* with an HSL value */
p { color: hsl(174,72%,56%) }

/* We now want our color to be 20% translucent which means a 80% opacity */

/* We can achieve this with an RGBa value */
p { color: rgba(64,224,208,0.8) }

/* Or an HSLa value */
p { color: hsla(174,72%,56%,0.8) }
```

[View live example](http://code.webplatform.org/gist/5502992)

## Usage

     Though CSS color values are precisely defined, they may appear differently between different output devices. Most of them are not calibrated, and some browsers do not support output device color profiles. Without these, color rendering may vary significantly.

## Notes

### Default color

Some browsers change the default color from black to another color in their default css (user-agent stylesheet).

### RGB, HSL, RGBa and HSLa support

HSL, RGBa and HSLa are not supported by older browsers (IE6-8), therefore if you do use such colours you should also provide a fallback color property that uses something similar but more widely supported, like a hex value. This should be placed either next to the modern color value but earlier in the cascade, or in a separate stylesheet hidden behind a conditional comment.

### Separating foreground from background

In order to make it easier for users to see and hear content including separating foreground from background, [[WCAG](http://www.w3.org/TR/2008/REC-WCAG20-20081211/)] indicates the following:

-   color is not used as the only visual means of conveying information, indicating an action, prompting a response, or distinguishing a visual element. [[Guideline 1.4.1](http://www.w3.org/TR/2008/REC-WCAG20-20081211/#visual-audio-contrast-without-color)] (Level A)
-   The visual presentation of text and images of text has a minimum contrast ratio of at least 4.5:1, with some exceptions. [[Contrast Minimum Guideline 1.4.3](http://www.w3.org/TR/2008/REC-WCAG20-20081211/#visual-audio-contrast-contrast)] (Level AA)
-   The visual presentation of text and images of text has an enhanced contrast ratio of at least 7:1 [[Guideline 1.4.6](http://www.w3.org/TR/2008/REC-WCAG20-20081211/#visual-audio-contrast7)] (Level AAA)

## Related specifications

Specification
:   Status
[CSS3 Color Module Level 3](http://www.w3.org/TR/css3-color/)
:   W3C Recommendation
[Color in CSS1](http://www.w3.org/TR/REC-CSS1/#color)
:   W3C Recommendation

## See also

### Other articles

-   [Setting color in CSS](/tutorials/setting_color_in_css)
-   [color](/css/color)
-   [color](/css/data_types/color)

-   [W3 css3-color Conformance Test Suite](http://www.w3.org/Style/CSS/Test/CSS3/Color/current/)
-   [MDN color property](https://developer.mozilla.org/en-US/docs/CSS/color)
-   [MSDN color property](http://msdn.microsoft.com/en-us/library/ie/ms530749(v=vs.85).aspx)

### css color value

See [css color value](/w/index.php?title=css/color/value&action=edit&redlink=1) for more information. The color value may be given as:

-   Basic color keyword

<!-- -->

    aqua, black, blue, fuchsia, gray, green, lime, maroon, navy, olive, purple, red, silver, teal, white, yellow

-   Extended color keyword

<!-- -->

    aliceblue, antiquewhite, aqua, aquamarine, azure, beige, bisque, black, blanchedalmond, ...

<dl>
<dd>
See [W3C CSS Color Module Recommendation 4.3. Extended color keywords](http://www.w3.org/TR/css3-color/#svg-color) for a complete list of keywords.

</dd>
</dl>
-   RGB

<!-- -->

    #00f
    #0000ff
    rgb(0,0,255)
    rgb(0%,0%,100%)

-   RGBA

<!-- -->

    rgba(0,0,255,0.5)
    rgba(0%,0%,100%,0.5)

-   HSL

<!-- -->

    hsl(0, 100%, 50%)

-   HSLA

<!-- -->

    hsla(0, 100%, 50%, 0.5)

-   "transparent" (since CSS3)
-   "currentColor" (since CSS3) (same as "color: inherit")
-   CSS2 system colors (Deprecated)
