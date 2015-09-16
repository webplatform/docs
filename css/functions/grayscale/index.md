---
title: 'grayscale()'
code_samples:
  - 'http://codepen.io/pverbeek/pen/iLyCE'
compatibility:
  feature: grayscale
  topic: css
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: "Converts an element's color to a shade of gray, for\nuse by the filter property. A decimal\nvalue between 0 and 1 or percentage up to 100% controls the extent of\nthe gray effect.\n"
tags:
  0: CSS
  1: Functions
  3: Graphics
  4: SVG
uri: css/functions/grayscale

---
## Summary

Converts an element's color to a shade of gray, for use by the filter property. A decimal value between 0 and 1 or percentage up to 100% controls the extent of the gray effect.

 This CSS property value is reflected in the following image:

    filter: grayscale(1);
    filter: grayscale(100%); /* same */

  ![f05-boatonlake.jpg](/assets/thumb/3/37/f05-boatonlake.jpg/300px-f05-boatonlake.jpg)![f06-boatonlakegray.jpg](/assets/thumb/7/7e/f06-boatonlakegray.jpg/300px-f06-boatonlakegray.jpg)

## Examples

The following example shows the difference between two images, where one has a grayscale of 75%. ![filter grayscale.png](/assets/thumb/8/88/filter_grayscale.png/400px-filter_grayscale.png)

``` html
<!DOCTYPE html>
<html>
  <head>
    <title>Filter example</title>
    <style>
      .foo {
        float: left;
      }

      .bar {
        -webkit-filter: grayscale(75%);
      }
    </style>
  </head>
  <body>
    <img src="http://www.webplatform.org/logo/wplogo_transparent_xlg.png" class="foo" />
    <img src="http://www.webplatform.org/logo/wplogo_transparent_xlg.png" class="foo bar" />
  </body>
</html>
```

[View live example](http://codepen.io/pverbeek/pen/iLyCE)

## Notes

The CSS filter corresponds to this SVG filter definition, based on a variable *amount* passed to the function:

``` xml
 <filter id="grayscale">
    <feColorMatrix type="matrix"
               values="(0.2126 + 0.7874 * [1 - amount]) (0.7152 - 0.7152 * [1 - amount]) (0.0722 - 0.0722 * [1 - amount]) 0 0
                       (0.2126 - 0.2126 * [1 - amount]) (0.7152 + 0.2848 * [1 - amount]) (0.0722 - 0.0722 * [1 - amount]) 0 0
                       (0.2126 - 0.2126 * [1 - amount]) (0.7152 - 0.7152 * [1 - amount]) (0.0722 + 0.9278 * [1 - amount]) 0 0
                       0 0 0 1 0"/>
  </filter>
```

## Related specifications

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

-   **grayscale()**

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
