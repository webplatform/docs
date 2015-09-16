---
title: 'drop-shadow()'
code_samples:
  - 'http://codepen.io/pverbeek/pen/etIyE'
  - 'http://codepen.io/pverbeek/pen/BlFef'
compatibility:
  feature: drop-shadow
  topic: css
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: "Applies a shadow to an element's pixels, for use by\nthe filter property.  Accepts up to 3\ndistance measurements, representing x/y offset and blur\nradius, along with a color value.\n"
tags:
  0: CSS
  1: Functions
  3: Graphics
  4: SVG
uri: css/functions/drop-shadow

---
## Summary

Applies a shadow to an element's pixels, for use by the filter property. Accepts up to 3 distance measurements, representing x/y offset and blur radius, along with a color value.

 This CSS property value is reflected in the following images:

    filter: drop-shadow(16px 16px 20px black);   /* left */
    filter: drop-shadow(10px -16px 30px purple); /* right */

  ![f23-mandrilldrop1.jpg](/assets/thumb/c/c2/f23-mandrilldrop1.jpg/300px-f23-mandrilldrop1.jpg)![f24-mandrillshadow2.jpg](/assets/thumb/a/a7/f24-mandrillshadow2.jpg/300px-f24-mandrillshadow2.jpg)

Setting offsets to 0 with a positive blur value produces a backlit halo effect. Setting blur to 0 and positive offset values produces a raised effect as if sunlight is falling on the element. The **drop-shadow()** function uses the same syntax as the [**text-shadow**](/css/properties/text-shadow) CSS property, and likewise allows for more than one set of shadow values, separated with commas. This example renders both of the shadows shown above:

    filter: drop-shadow(16px 16px 20px black, 10px -16px 30px purple);

The filter affects the contours of image transparencies, which allows for more vivid shadow effects:

![giraffe dropshadow.png](/assets/public/8/82/giraffe_dropshadow.png)

## Examples

The below example shows the difference between the CSS box-shadow property and the drop-shadow filter function. Where the box-shadow property outlines the html box and the drop-shadow outlines the element parts.

``` html
<!DOCTYPE html>
<html>
  <head>
    <title>Filter example</title>
    <style>
      .foo {
        width: 100px;
        padding: 50px 0;
        margin: 100px;
        text-align: center;
        border: dashed 10px red;
        float: left;
      }

      .bar {
        box-shadow: 5px 5px 10px black;
      }

      .baz {
        -webkit-filter: drop-shadow(5px 5px 10px black);
      }
    </style>
  </head>
  <body>
    <div class="foo bar"></div>
    <div class="foo baz"></div>
  </body>
</html>
```

[View live example](http://codepen.io/pverbeek/pen/etIyE)

This example shows the difference when using png images with transparency.

![filter dropshadow.png](/assets/thumb/7/78/filter_dropshadow.png/400px-filter_dropshadow.png)

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
        box-shadow: 5px 5px 10px black;
      }

      .baz {
        -webkit-filter: drop-shadow(5px 5px 10px black);
      }
    </style>
  </head>
  <body>
    <img src="http://www.webplatform.org/logo/wplogo_transparent_xlg.png" class="foo" />
    <img src="http://www.webplatform.org/logo/wplogo_transparent_xlg.png" class="foo bar" />
  </body>
  </body>
</html>
```

[View live example](http://codepen.io/pverbeek/pen/BlFef)

## Notes

The CSS filter corresponds to this SVG filter definition, based on variable *offset-x*, *offset-y*, blur *radius*, and *color* values passed to the function:

``` xml
<filter id="drop-shadow">
  <feGaussianBlur in="[alpha-channel-of-input]" stdDeviation="[radius]"/>
  <feOffset dx="[offset-x]" dy="[offset-y]" result="offsetblur"/>
  <feFlood flood-color="[color]"/>
  <feComposite in2="offsetblur" operator="in"/>
  <feMerge>
    <feMergeNode/>
    <feMergeNode in="[input-image]"/>
  </feMerge>
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

-   **drop-shadow()**

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

-   W3C editor's draft: [Filter Effects 1.0](https://dvcs.w3.org/hg/FXTF/raw-file/tip/filters/index.html#)
-   [Interactive demonstration](http://html5-demos.appspot.com/static/css/filters/index.html)
