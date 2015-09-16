---
title: 'cursor'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/).'
  - 'Microsoft Developer Network.'
code_samples:
  - 'https://gist.github.com/9b54d2d8dc9bc94382d5'
compatibility:
  feature: cursor
  topic: css
notes:
  - 'Add example, description, specifications, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'all elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified (if a keyword), URLs are converted to absolute'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`cursor`'
  Percentages: N/A
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'The cursor CSS property specifies the mouse cursor displayed when the mouse pointer is over an element.'
tags:
  - CSS
  - Properties
uri: css/properties/cursor

---
## Summary

The cursor CSS property specifies the mouse cursor displayed when the mouse pointer is over an element.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `auto`

Applies to
:   all elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified (if a keyword), URLs are converted to absolute

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `cursor`

Percentages
:   N/A

## Syntax

-   `cursor: standard values`
-   `cursor: url() hotspot-x hotspot-y, keyword;`
-   `cursor: url(), keyword`

## Values

standard values
:   There are many standard cursors available:

-   `auto`
-   `default`
-   `none`
-   `context-menu`
-   `help`
-   `pointer`
-   `progress`
-   `wait`
-   `cell`
-   `crosshair`
-   `text`
-   `vertical-text`
-   `alias`
-   `copy`
-   `move`
-   `no-drop`
-   `not-allowed`
-   `e-resize`
-   `n-resize`
-   `ne-resize`
-   `nw-resize`
-   `s-resize`
-   `se-resize`
-   `sw-resize`
-   `w-resize`
-   `ew-resize`
-   `ns-resize`
-   `nesw-resize`
-   `nwse-resize`
-   `col-resize`
-   `row-resize`
-   `all-scroll`
-   `zoom-in`
-   `zoom-out`

These have varying support across different browsers — see the support section. The examples below feature different boxes with different cursor values set on them, so you can get an idea of what the different ones look like.

url(), keyword
:   Instead of specifying a standard pointer type, you can specify a `url()` function pointing to a custom graphic to use as a cursor, which must be followed by a fallback keyword to use as a pointer if the image is not available (this can be `auto` or a standard keyword value). For example, `cursor: url(), auto;`

You can supply multiple `url()` functions separated by commas (`url(), url(), auto` for example), and the browser will use the earliest appropriate image it can find. Limitations include:

-   Cursor size: if the cursor image is over a certain size it will be ignored (in Gecko for example the limit is 128×128px). You should limit yourself about 32×32px anyway, for maximum compatibility with operating systems and platforms.
-   Browser: In Opera, the custom cursors are just ignored, and the keywords are used instead.
-   Transparency: Translucent cursors are not supported on Windows releases earlier than XP. This is a limitation of the operating system. Transparency works on all platforms.
-   Image format: Most browsers support a wide variety of image formats, but you should stick to something common and web-optimizable for the most part, such as JPG or PNG. You'll also need to include a CUR format image, as they are required by IE. Animateds PNGs and GIFs will only produce static cursors.

url() hotspot-x hotspot-y, keyword;
:   CSS3 allows you to specify a custom cusor image along with an X and Y number values for the pointer hotspot, for example `cursor:  url(cursor2.png) 2 2, auto;`. If not specified, the hotspot position defaults to the top left corner of the cursor image, or may be read from the meta data inside the image file, in the case of CUR and XBM format files.

## Examples

To make the cursor appear like it's busy

``` css
.busy  {
    cursor: wait;
}
```

[View live example](https://code.webplatform.org/gist/9b54d2d8dc9bc94382d5)

## See also

### Related articles

#### Visual Effects

-   [color](/css/color)

-   [Colors by Hue](/css/color/colors_by_hue)

-   [Colors by Name](/css/color/colors_by_name)

-   [Colors by Saturation](/css/color/colors_by_saturation)

-   [User-Defined System Colors](/css/color/user-defined_system_colors)

-   [-ms-high-contrast](/css/high_contrast_mode/properties/-ms-high-contrast)

-   [ms-high-contrast-adjust](/css/high_contrast_modeapis/properties/ms-high-contrast-adjust)

-   [-ms-progress-appearance](/css/properties/-ms-progress-appearance)

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [clip](/css/properties/clip)

-   **cursor**

-   [opacity](/css/properties/opacity)

-   [zoom](/css/properties/zoom)

-   [height](/html/attributes/height)

-   [blink](/html/elements/blink)

-   [filter](/svg/elements/filter)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)
