---
title: filter
code_samples:
  - 'http://gist.github.com/5842451'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`filter`'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Applies various image processing effects.  This property is largely unsupported.  See Compatibility section for more information.'
tags:
  0: CSS
  1: Properties
  3: Graphics
  4: SVG
uri: css/properties/filter

---
## Summary

Applies various image processing effects. This property is largely unsupported. See Compatibility section for more information.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `none`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `filter`

## Syntax

-   `filter: <function>`
-   `filter: url(path/to/filter.svg#filterID)`

## Values

\<function\>
:   Any combination of built-in filter functions: [**blur()**](/css/functions/blur), [**brightness()**](/css/functions/brightness), [**contrast()**](/css/functions/contrast), [**custom()**](/css/functions/custom), [**drop-shadow()**](/css/functions/drop-shadow), [**grayscale()**](/css/functions/grayscale), [**hue-rotate()**](/css/functions/hue-rotate), [**invert()**](/css/functions/invert), [**opacity()**](/css/functions/opacity), [**saturate()**](/css/functions/saturate), and [**sepia()**](/css/functions/sepia)

url(path/to/filter.svg\#filterID)
:   A reference to an [SVG \<filter\> element](/svg/elements/filter)

## Examples

The example below shows the difference between the CSS box-shadow property and the drop-shadow filter function. The box-shadow property outlines the html box and the drop-shadow outlines the element parts.

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

[View live example](http://code.webplatform.org/gist/5842451)

## Usage

     Filters apply any combination of image processing functions to

visual elements. This example shows how a combination of more than one filter function may affect an image:

    filter: grayscale(100%) sepia(100%);

  ![f01-pencil.jpg](/assets/thumb/a/a8/f01-pencil.jpg/300px-f01-pencil.jpg)![f04-graysepia.jpg](/assets/thumb/2/25/f04-graysepia.jpg/300px-f04-graysepia.jpg)

Filters are applied to the image data in sequence, so the order in which functions are declared makes a difference. If the [**sepia()**](/css/functions/sepia) function were applied before the [**grayscale()**](/css/functions/grayscale) in the example above, the image would appear completely gray rather than slightly yellowed.

Filters apply to any graphic effect the element renders, such as borders, background images, scrollbars, letterforms, text selections, even videos. Each filter also applies to the cumulative effect of previously declared filters (the same function may be applied repeatedly). Both the [**blur()**](/css/functions/blur) and [**drop-shadow()**](/css/functions/drop-shadow) filters may render pixels outside the original content box, and when paired with other CSS properties such as [**opacity**](/css/properties/opacity), these pixels may become clipped.

Filter effects may be specified as part of dynamic [transitions](/tutorials/css_transitions#advanced) and [keyframe animations](/tutorials/css_animations). However, the number of functions in each set of style sheets must match, with no transitions allowed from implied default values. In addition, each style sheet must declare the exact same sequence of functions.

## Built-in filter functions

The following examples show the effect of each filter function applied in isolation. See each function for details on accepted parameters.

[**brightness(1.4)**](/css/functions/brightness)

  ![f17-boatonlake2.jpg](/assets/thumb/1/15/f17-boatonlake2.jpg/300px-f17-boatonlake2.jpg)![f18-boatonlake2bright.jpg](/assets/thumb/6/67/f18-boatonlake2bright.jpg/300px-f18-boatonlake2bright.jpg)

[**contrast(2)**](/css/functions/contrast)

  ![f19-jellybeans.jpg](/assets/public/b/b5/f19-jellybeans.jpg)![f20-jellybeancontrast.jpg](/assets/public/a/a5/f20-jellybeancontrast.jpg)

[**grayscale(1)**](/css/functions/grayscale)

  ![f05-boatonlake.jpg](/assets/thumb/3/37/f05-boatonlake.jpg/300px-f05-boatonlake.jpg)![f06-boatonlakegray.jpg](/assets/thumb/7/7e/f06-boatonlakegray.jpg/300px-f06-boatonlakegray.jpg)

[**sepia(1)**](/css/functions/sepia)

  ![f07-lenna.jpg](/assets/thumb/e/e6/f07-lenna.jpg/300px-f07-lenna.jpg)![f08-lennasepia.jpg](/assets/thumb/7/70/f08-lennasepia.jpg/300px-f08-lennasepia.jpg)

[**invert(1)**](/css/functions/invert)

  ![f13-peppers.jpg](/assets/thumb/1/11/f13-peppers.jpg/300px-f13-peppers.jpg)![f14-peppersinvert.jpg](/assets/thumb/1/19/f14-peppersinvert.jpg/300px-f14-peppersinvert.jpg)

[**hue-rotate(90deg)**](/css/functions/hue-rotate)

  ![f11-mandrill.jpg](/assets/thumb/8/80/f11-mandrill.jpg/300px-f11-mandrill.jpg)![f12-mandrillhuerotate.jpg](/assets/thumb/d/d5/f12-mandrillhuerotate.jpg/300px-f12-mandrillhuerotate.jpg)

[**saturate(10)**](/css/functions/saturate)

  ![f09-tiffany.jpg](/assets/thumb/2/2d/f09-tiffany.jpg/300px-f09-tiffany.jpg)![f10-tiffanysaturate.jpg](/assets/thumb/b/be/f10-tiffanysaturate.jpg/300px-f10-tiffanysaturate.jpg)

[**opacity(0.5)**](/css/functions/opacity)

  ![f15-splash.jpg](/assets/thumb/0/04/f15-splash.jpg/300px-f15-splash.jpg)![f16-splashopacity50.jpg](/assets/public/6/68/f16-splashopacity50.jpg)

[**blur(10px)**](/css/functions/blur)

  ![f21-peppers2.jpg](/assets/thumb/a/ad/f21-peppers2.jpg/300px-f21-peppers2.jpg)![f22-peppers2blur.jpg](/assets/thumb/5/52/f22-peppers2blur.jpg/300px-f22-peppers2blur.jpg)

[**drop-shadow(16px 16px 20px black)**](/css/functions/drop-shadow)

  ![f11-mandrill.jpg](/assets/thumb/8/80/f11-mandrill.jpg/300px-f11-mandrill.jpg)![f23-mandrilldrop1.jpg](/assets/thumb/c/c2/f23-mandrilldrop1.jpg/300px-f23-mandrilldrop1.jpg)

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

-   [opacity()](/css/functions/opacity)

-   [saturate()](/css/functions/saturate)

-   [sepia()](/css/functions/sepia)

-   **filter**

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
-   [HTML5 Rocks! Understanding CSS Filters article](http://www.html5rocks.com/en/tutorials/filters/understanding-css/)
