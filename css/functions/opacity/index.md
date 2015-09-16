---
title: 'opacity()'
code_samples:
  - 'http://codepen.io/pverbeek/pen/qhfaD'
  - 'http://codepen.io/pverbeek/pen/KzEHw'
compatibility:
  feature: opacity
  topic: css
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: "Applies a transparency effect to an element's\ncolors, for use by the filter\nproperty. A decimal value between 0 and 1 or percentage up to 100%\ncontrols the overall opacity, with 0 rendering the element invisible\nand background elements showing through.\n"
tags:
  0: CSS
  1: Functions
  3: Graphics
  4: SVG
uri: css/functions/opacity

---
## Summary

Applies a transparency effect to an element's colors, for use by the filter property. A decimal value between 0 and 1 or percentage up to 100% controls the overall opacity, with 0 rendering the element invisible and background elements showing through.

 This CSS property value is reflected in the following image:

    filter: opacity(50%);
    filter: opacity(0.5);

  ![f15-splash.jpg](/assets/thumb/0/04/f15-splash.jpg/300px-f15-splash.jpg)![f16-splashopacity50.jpg](/assets/public/6/68/f16-splashopacity50.jpg)

When used in isolation, the **opacity()** filter has the same effect as the [**opacity**](/css/properties/opacity) CSS property, but it produces different effects when used in conjunction with other filters. The second example below produces a shadow that shows through the image, and the third doesn't when functions execute in reverse order:

    filter: none;
    filter: opacity(0.5) drop-shadow(10px 10px 0px black);
    filter: drop-shadow(10px 10px 0px black) opacity(0.5);

![opacitySequence.png](/assets/public/8/80/opacitySequence.png)

**Note:** As is true for the related [**opacity**](/css/properties/opacity) CSS property, transparent elements still receive mouse and touch events, but the [**pointer-events**](/css/properties/pointer-events) property offers a way to override this behavior.

## Examples

The following example shows the difference between two images, where one has an opacity of 50%:

![filter opacity1.png](/assets/thumb/0/09/filter_opacity1.png/400px-filter_opacity1.png)

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
        -webkit-filter: opacity(50%);
      }
    </style>
  </head>
  <body>
    <img src="http://www.webplatform.org/logo/wplogo_transparent_xlg.png" class="foo" />
    <img src="http://www.webplatform.org/logo/wplogo_transparent_xlg.png" class="foo bar" />
  </body>
</html>
```

[View live example](http://codepen.io/pverbeek/pen/qhfaD)

This example shows the importance of the order in which filters are applied. In the first image, the opacity is only applied to the image. In the second, the drop-shadow is applied first, so the opacity also applies to it.

![filter opacity2.png](/assets/thumb/c/c4/filter_opacity2.png/400px-filter_opacity2.png)

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
        -webkit-filter: opacity(.5) drop-shadow(1px 1px 20px black);
      }

      .baz {
        -webkit-filter: drop-shadow(1px 1px 20px black) opacity(.5);
      }
    </style>
  </head>
  <body>
    <img src="http://www.webplatform.org/logo/wplogo_transparent_xlg.png" class="foo bar" />
    <img src="http://www.webplatform.org/logo/wplogo_transparent_xlg.png" class="foo baz" />
  </body>
</html>
```

[View live example](http://codepen.io/pverbeek/pen/KzEHw)

## Notes

The CSS filter corresponds to this SVG filter definition, based on a variable *amount* passed to the function:

``` xml
<filter id="opacity">
  <feComponentTransfer>
    <feFuncA type="table" tableValues="0 [amount]"/>
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

-   [invert()](/css/functions/invert)

-   **opacity()**

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
