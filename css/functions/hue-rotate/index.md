---
title: hue-rotate
tags:
  0: CSS
  1: Functions
  3: Graphics
  4: SVG
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: "Shifts an element's relative hue, for use by the\nfilter property. Accepts either a\ndeg or rad angle measurement representing a wheel of hues.\n"
code_samples:
  - 'http://codepen.io/pverbeek/pen/axEbp'
uri: css/functions/hue-rotate

---
# hue-rotate()

## Summary

Shifts an element's relative hue, for use by the filter property. Accepts either a deg or rad angle measurement representing a wheel of hues.

 This CSS property value is reflected in the following image:

    filter: hue-rotate(90deg);

  ![f11-mandrill.jpg](/assets/thumb/8/80/f11-mandrill.jpg/300px-f11-mandrill.jpg)![f12-mandrillhuerotate.jpg](/assets/thumb/d/d5/f12-mandrillhuerotate.jpg/300px-f12-mandrillhuerotate.jpg)

Specifying measurements greater than 360° (or 2π **rad**) allows animations to cycle more than once around the color wheel. This example cycles colors three times, returning to its original set of hues (360 × 3):

    @keyframes spinCycle {
        from { filter: hue-rotate(0deg)    }
        to   { filter: hue-rotate(1080deg) }
    }

## Examples

The following example shows the difference between two images, where one has a hue rotation of 180 degrees.

![filter huerotate.png](/assets/thumb/9/9d/filter_huerotate.png/400px-filter_huerotate.png)

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
        -webkit-filter: hue-rotate(180deg);
      }
    </style>
  </head>
  <body>
    <img src="http://www.webplatform.org/logo/wplogo_transparent_xlg.png%22 class="foo" />
    <img src="http://www.webplatform.org/logo/wplogo_transparent_xlg.png%22 class="foo bar" />
  </body>
</html>
```

[View live example](http://codepen.io/pverbeek/pen/axEbp)

## Notes

The CSS filter corresponds to this SVG filter definition, based on a variable *angle* passed to the function:

``` {.xml}
<filter id="hue-rotate">
  <feColorMatrix type="hueRotate" values="[angle]"/>
</filter>
```

 Note that the hue rotation algorithm for CSS filters only approximates a hue-rotation in HSL - the content is never actually converted to the HSL color space. This results in brightness and saturation clipping for saturated colors in certain ranges. For example, pure RGB colors, such as rgb(255,0,0), do not produce expected results, especially between 0 and 90 degrees. A comparison of manually rotated colors (outer ring) made by explicitly defining HSL colors, and their hue-rotate() equivalent (inner ring) using a base of pure RGB red (HSL equivalent: 0,100%,50%) is shown below. As you can see, the 60 degree hue rotation that should produce a bright saturated yellow, instead produces a color of the correct hue, but incorrect saturation and brightness.

 ![saturated hue rotation.JPG](/assets/thumb/d/d4/saturated_hue_rotation.JPG/400px-saturated_hue_rotation.JPG)

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

-   [brightness()](/css/functions/brightness)

-   [contrast()](/css/functions/contrast)

-   [custom()](/css/functions/custom)

-   [drop-shadow()](/css/functions/drop-shadow)

-   [grayscale()](/css/functions/grayscale)

-   **hue-rotate()**

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

