---
title: blur()
code_samples:
  - 'http://codepen.io/pverbeek/pen/yiKBv'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: "Blurs an element, for use by the\nfilter property.  Accepts a distance\nmeasurement within which pixels are randomly scattered. A value of 0\nleaves the image as is.\n"
tags:
  0: CSS
  1: Functions
  3: Graphics
  4: SVG
uri: css/functions/blur

---
## <span>Summary</span>

Blurs an element, for use by the filter property. Accepts a distance measurement within which pixels are randomly scattered. A value of 0 leaves the image as is.

 This CSS property value is reflected in the following image:

    filter: blur(10px);

  ![f21-peppers2.jpg](/assets/thumb/a/ad/f21-peppers2.jpg/300px-f21-peppers2.jpg)![f22-peppers2blur.jpg](/assets/thumb/5/52/f22-peppers2blur.jpg/300px-f22-peppers2blur.jpg)

Note that pixels blur around the contours of image transparencies, possibly affecting the ability of background content to show through:

![music blur.png](/assets/public/2/25/music_blur.png)

## <span>Examples</span>

The following example shows the difference between two images, where one has a blur of 10px: ![filter blur.png](/assets/thumb/7/78/filter_blur.png/400px-filter_blur.png)

``` html
<!DOCTYPE html>
<html>
  <head>
    <title>Blur example</title>
    <style>
      .foo {
        float: left;
      }

      .bar {
        -webkit-filter: blur(10px);
      }
   </style>
  </head>
  <body>
    <img src="http://www.webplatform.org/logo/wplogo_transparent_xlg.png" class="foo" />
    <img src="http://www.webplatform.org/logo/wplogo_transparent_xlg.png" class="foo bar" />
  </body>
</html>
```

[View live example](http://codepen.io/pverbeek/pen/yiKBv)

## <span>Notes</span>

The CSS filter corresponds to this SVG filter definition, based on a variable *radius* passed to the function:

``` xml
<filter id="blur">
  <feGaussianBlur stdDeviation="[radius radius]">
</filter>
```

## <span>Related specifications</span>

[Filter Effects 1.0](https://dvcs.w3.org/hg/FXTF/raw-file/tip/filters/index.html#)
:   Editor's Draft

[Filter Effects 1.0](http://www.w3.org/TR/filter-effects/)
:   Working Draft

## <span>See also</span>

### <span>Related articles</span>

#### <span>Filters</span>

-   **blur()**

-   [brightness()](/css/functions/brightness)

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

### <span>External resources</span>

-   [Adobe CSS FilterLab](http://html.adobe.com/webstandards/csscustomfilters/cssfilterlab/)
-   [Interactive demonstration](http://html5-demos.appspot.com/static/css/filters/index.html)
