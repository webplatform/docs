---
title: brightness
tags:
  0: CSS
  1: Functions
  3: Graphics
  4: SVG
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Adjust the brightness of an element''s color, for use by the filter property.  A value of 100% or decimal value of 1 leaves the image as is, while 0 produces black.  Increasing the value from 1 or 100% brightens pixels from their original values.'
code_samples:
  - 'http://codepen.io/pverbeek/pen/Aamdu'
uri: css/functions/brightness

---
# brightness()

## Summary

Adjust the brightness of an element's color, for use by the filter property. A value of 100% or decimal value of 1 leaves the image as is, while 0 produces black. Increasing the value from 1 or 100% brightens pixels from their original values.

 This CSS property value is reflected in the following image:

    filter: brightness(40%);
    filter: brightness(0.4); /* same */

  ![f17-boatonlake2.jpg](/assets/thumb/1/15/f17-boatonlake2.jpg/300px-f17-boatonlake2.jpg)![f18-boatonlake2bright.jpg](/assets/thumb/6/67/f18-boatonlake2bright.jpg/300px-f18-boatonlake2bright.jpg)

## Examples

The following example shows the difference between two images, where one has a brightness of 50%: ![filter brightness.png](/assets/thumb/c/c9/filter_brightness.png/400px-filter_brightness.png)

``` {.html}
<!DOCTYPE html>
<html>
  <head>
    <title>Filter example</title>
    <style>
      .foo {
        float: left;
      }

      .bar {
        -webkit-filter: brightness(50%);
      }
    </style>
  </head>
  <body>
    <img src="http://www.webplatform.org/logo/wplogo_transparent_xlg.png%22 class="foo" />
    <img src="http://www.webplatform.org/logo/wplogo_transparent_xlg.png%22 class="foo bar" />
  </body>
</html>
```

[View live example](http://codepen.io/pverbeek/pen/Aamdu)

## Notes

The CSS filter corresponds to this SVG filter definition, based on a variable *amount* passed to the function:

``` {.xml}
<filter id="brightness">
  <feComponentTransfer>
    <feFuncR type="linear" slope="[amount]"/>
    <feFuncG type="linear" slope="[amount]"/>
    <feFuncB type="linear" slope="[amount]"/>
  </feComponentTransfer>
</filter>
```

## Related specifications

Specification
:   Status
[Filter Effects 1.0](https://dvcs.w3.org/hg/FXTF/raw-file/tip/filters/index.html#)
:   Editor's Draft
[Filter Effects 1.0](http://www.w3.org/TR/filter-effects/)
:   Working Draft

## See also

### Related articles

#### Filters

-   [blur()](/css/functions/blur)

-   **brightness()**

-   [contrast()](/css/functions/contrast)

-   [custom()](/css/functions/custom)

-   [drop-shadow()](/css/functions/drop-shadow)

-   [grayscale()](/css/functions/grayscale)

-   [hue-rotate()](/css/functions/hue-rotate)

-   [invert()](/css/functions/invert)

-   [opacity()](/css/functions/opacity)

-   [saturate()](/css/functions/saturate)

-   [sepia()](/css/functions/sepia)

-   [filter](/css/properties/filter)

-   [feBlend](/svg/elements/feBlend)

-   [feColorMatrix](/svg/elements/feColorMatrix)

-   [feComponentTransfer](/svg/elements/feComponentTransfer)

-   [feComposite](/svg/elements/feComposite)

-   [feConvolveMatrix](/svg/elements/feConvolveMatrix)

-   [feDiffuseLighting](/svg/elements/feDiffuseLighting)

-   [feDisplacementMap](/svg/elements/feDisplacementMap)

-   [feDistantLight](/svg/elements/feDistantLight)

-   [feFlood](/svg/elements/feFlood)

-   [feFuncA](/svg/elements/feFuncA)

-   [feFuncB](/svg/elements/feFuncB)

-   [feFuncG](/svg/elements/feFuncG)

-   [feFuncR](/svg/elements/feFuncR)

-   [feGaussianBlur](/svg/elements/feGaussianBlur)

-   [feImage](/svg/elements/feImage)

-   [feMerge](/svg/elements/feMerge)

-   [feMergeNode](/svg/elements/feMergeNode)

-   [feMorphology](/svg/elements/feMorphology)

-   [feOffset](/svg/elements/feOffset)

-   [fePointLight](/svg/elements/fePointLight)

-   [feSpecularLighting](/svg/elements/feSpecularLighting)

-   [feSpotlight](/svg/elements/feSpotlight)

-   [feTile](/svg/elements/feTile)

-   [feTurbulence](/svg/elements/feTurbulence)

-   [SVG deployment](/svg/tutorials/smarter_svg_deploy)

-   [SVG filters](/svg/tutorials/smarter_svg_filters)

-   [SVG graphic effects](/svg/tutorials/smarter_svg_graphics)

-   [SVG grand tour](/svg/tutorials/smarter_svg_overview)

-   [SVG filters](/tutorials/svg_filters)

### External resources

-   [Adobe CSS FilterLab](http://html.adobe.com/webstandards/csscustomfilters/cssfilterlab/)
-   [Interactive demonstration](http://html5-demos.appspot.com/static/css/filters/index.html)

