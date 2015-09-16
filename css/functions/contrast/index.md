---
title: 'contrast()'
code_samples:
  - 'http://codepen.io/pverbeek/pen/xzBlg'
compatibility:
  feature: contrast
  topic: css
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: "Adjusts the difference between light and dark\nvalues, for use by the filter\nproperty.  A value of 100% or a decimal value of 1 leaves the image as\nis, while 0 results in black. Increasing the value past 1 or 100%\nproduces more dramatically stratified areas of light and dark.\n"
tags:
  0: CSS
  1: Functions
  3: Graphics
  4: SVG
uri: css/functions/contrast

---
## Summary

Adjusts the difference between light and dark values, for use by the filter property. A value of 100% or a decimal value of 1 leaves the image as is, while 0 results in black. Increasing the value past 1 or 100% produces more dramatically stratified areas of light and dark.

 This CSS property value is reflected in the following image:

    filter: contrast(200%);
    filter: contrast(2); /* same */

  ![f19-jellybeans.jpg](/assets/public/b/b5/f19-jellybeans.jpg)![f20-jellybeancontrast.jpg](/assets/public/a/a5/f20-jellybeancontrast.jpg)

## Examples

The following example shows the difference between three images, the first has the default contrast, the second one a lower contrast and the third a higher:

![filter contrast.png](/assets/thumb/5/56/filter_contrast.png/400px-filter_contrast.png)

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
        -webkit-filter: contrast(50%);
      }

      .baz {
        -webkit-filter: contrast(1.5);
      }
    </style>
  </head>
  <body>
    <img src="http://www.webplatform.org/logo/wplogo_transparent_xlg.png" class="foo" />
    <img src="http://www.webplatform.org/logo/wplogo_transparent_xlg.png" class="foo bar" />
    <img src="http://www.webplatform.org/logo/wplogo_transparent_xlg.png" class="foo baz" />
  </body>
</html>
```

[View live example](http://codepen.io/pverbeek/pen/xzBlg)

## Notes

The CSS filter corresponds to this SVG filter definition, based on a variable *amount* passed to the function:

``` xml
<filter id="contrast">
  <feComponentTransfer>
    <feFuncR type="linear" slope="[amount]" intercept="-(0.5 * [amount] + 0.5)"/>
    <feFuncG type="linear" slope="[amount]" intercept="-(0.5 * [amount] + 0.5)"/>
    <feFuncB type="linear" slope="[amount]" intercept="-(0.5 * [amount] + 0.5)"/>
  </feComponentTransfer>
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

-   **contrast()**

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
