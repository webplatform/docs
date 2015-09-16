---
title: 'custom()'
code_samples:
  - 'http://codepen.io/pverbeek/pen/piKgC'
compatibility:
  feature: custom
  topic: css
notes:
  - 'Light in content compared to the others, but makes sense as custom. May want to provide elaboration in the future.'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'With CSS custom filters you can create your own sophisticated effects on DOM elements. They work with CSS animations and transitions to create complex animated visual effects.'
tags:
  0: CSS
  1: Functions
  3: Graphics
  4: SVG
uri: css/functions/custom

---
## Summary

With CSS custom filters you can create your own sophisticated effects on DOM elements. They work with CSS animations and transitions to create complex animated visual effects.

## Examples

Using shaders created by Adobe, the following example shows how to create a folded map effect with custom CSS filters.

``` html
<!DOCTYPE html>
<html>
<head>
  <style>
    #map {
      width: 400px;
      height: 400px;
      -webkit-transform: translate3d(0px, 0px, 0px);
      -webkit-filter: custom(
        url(http://html.adobe.com/webstandards/csscustomfilters/cssfilterlab/shaders/vertex/fold.vs) mix(url(http://html.adobe.com/webstandards/csscustomfilters/cssfilterlab/shaders/fragment/fold.fs) multiply source-atop),
        8 50,
        transform perspective(1000) scale(1) rotateX(0deg) rotateY(0deg) rotateZ(0deg),
        t 0.5,
        spins 1.5,
        phase -0.7,
        shadow 1.5,
        mapDepth 40,
        mapCurve -0.3,
        minSpacing 0.3,
        useColoredBack 1,
        backColor 0.5 0.5 0.5 1
      );
    }
  </style>
</head>
<body>
  <img src="http://maps.googleapis.com/maps/api/staticmap?center=51.58803,4.774246&zoom=15&size=400x400&sensor=false" id="map" />
</body>
</html>
```

[View live example](http://codepen.io/pverbeek/pen/piKgC)

## See also

### Related articles

#### Filters

-   [blur()](/css/functions/blur)

-   [brightness()](/css/functions/brightness)

-   [contrast()](/css/functions/contrast)

-   **custom()**

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

-   [OpenGL ES Shading Language (PDF)](http://www.khronos.org/files/opengles_shading_language.pdf)
-   [Adobe CSS FilterLab](http://html.adobe.com/webstandards/csscustomfilters/cssfilterlab/)
-   [Introducing CSS shaders](http://www.adobe.com/devnet/html5/articles/css-shaders.html)
