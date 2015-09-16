---
title: invert()
code_samples:
  - 'http://codepen.io/pverbeek/pen/Dlpta'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: "Flips an element's colors, for use by the\nfilter property.  A decimal value\nbetween 0 and 1 or percentage up to 100% controls the extent of the\ncolor-negative effect, with 0.5 or 50% producing gray.\n"
tags:
  0: CSS
  1: Functions
  3: Graphics
  4: SVG
uri: css/functions/invert

---
## Summary

Flips an element's colors, for use by the filter property. A decimal value between 0 and 1 or percentage up to 100% controls the extent of the color-negative effect, with 0.5 or 50% producing gray.

 This CSS property value is reflected in the following image:

    filter: invert(100%);
    filter: invert(1); /* same */

  ![f13-peppers.jpg](/assets/thumb/1/11/f13-peppers.jpg/300px-f13-peppers.jpg)![f14-peppersinvert.jpg](/assets/thumb/1/19/f14-peppersinvert.jpg/300px-f14-peppersinvert.jpg)

## Examples

The following example shows the difference between two images, where one has a been inverted for 75%:

![filter invert.png](/assets/thumb/d/d0/filter_invert.png/400px-filter_invert.png)

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
        -webkit-filter: invert(75%);
      }
    </style>
  </head>
  <body>
    <img src="http://www.webplatform.org/logo/wplogo_transparent_xlg.png" class="foo" />
    <img src="http://www.webplatform.org/logo/wplogo_transparent_xlg.png" class="foo bar" />
  </body>
</html>
```

[View live example](http://codepen.io/pverbeek/pen/Dlpta)

## Notes

The CSS filter corresponds to this SVG filter definition, based on a variable *amount* passed to the function:

``` xml
<filter id="invert">
  <feComponentTransfer>
    <feFuncR type="table" tableValues="[amount] (1 - [amount])"/>
    <feFuncG type="table" tableValues="[amount] (1 - [amount])"/>
    <feFuncB type="table" tableValues="[amount] (1 - [amount])"/>
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

-   [contrast()](/css/functions/contrast)

-   [custom()](/css/functions/custom)

-   [drop-shadow()](/css/functions/drop-shadow)

-   [grayscale()](/css/functions/grayscale)

-   [hue-rotate()](/css/functions/hue-rotate)

-   **invert()**

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
