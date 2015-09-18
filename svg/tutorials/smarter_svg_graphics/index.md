---
title: 'SVG graphic effects'
notes:
  - 'Fix multiple broken links'
readiness: 'In Progress'
summary: 'This guide shows you how to embed images within SVG and apply various graphics effects such as gradients, patterns, clipping paths, and masks.'
tags:
  - Tutorials
  - SVG
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - svg/properties/fill
    - svg/properties/stop-color
    - svg/attributes/offset
    - svg/attributes/gradientUnits
    - svg/attributes/fx
    - svg/attributes/fy
    - svg/attributes/cx
    - svg/attributes/cy
    - svg/attributes/r
    - svg/attributes/width
    - svg/attributes/height
    - svg/attributes/x
    - svg/attributes/y
    - svg/attributes/transform
    - svg/attributes/patternTransform
    - svg/properties/clip-path
    - svg/attributes/preserveAspectRatio
    - svg/attributes/viewBox
uri: 'svg/tutorials/smarter svg graphics'

---
**By Mike Sierra**

## Summary

This guide shows you how to embed images within SVG and apply various graphics effects such as gradients, patterns, clipping paths, and masks.

## Gradients

SVG's support for gradients is similar to CSS's. Two kinds of gradient are available: the [**linearGradient**](/svg/elements/linearGradient) and [**radialGradient**](/svg/elements/radialGradient) elements. The [**fill**](/w/index.php?title=svg/properties/fill&action=edit&redlink=1) property uses **url()** syntax to reference either kind:

``` xml
<path id="tvScreen" fill="url(#tvScreenOff)" d="M159.957 184.103c-21.826 13.892-102.52 17.859-122.361 0c-19.843-17.857-22.486-83.999 0-99.873c22.489-15.874 104.504-17.858 122.361 0C177.814 102.088 181.783 170.214 159.957 184.103z"/>
```

 This example transitions from a light to a dark gray from the top to the bottom of the shape:

``` xml
<linearGradient id="tvScreenOff" x1="0" y1="0" x2="0" y2="1" >
    <stop offset="0" stop-color="#dddddd" />
    <stop offset="1" stop-color="#444444" />
</linearGradient>
```

 ![svg gfx gradient linear bw.png](//static.webplatform.org/thumb/a/a8/svg_gfx_gradient_linear_bw.png/200px-svg_gfx_gradient_linear_bw.png)

In their simplest form, gradients require at least two nested [**stop**](/svg/elements/stop) elements to transition between their [**stop-color**](/w/index.php?title=svg/properties/stop-color&action=edit&redlink=1) properties. The [**offset**](/w/index.php?title=svg/attributes/offset&action=edit&redlink=1) attribute specifies the progression of colors, either in percentage or corresponding decimal terms. That progression follows the line defined by the [**linearGradient**](/svg/elements/linearGradient) element's pair of *x* and *y* coordinates. If **y1** were 1 in this example, the gradient would shift from the top left to the bottom right.

This example defines many more colors, progressing from bottom to top. Setting [**gradientUnits**](/w/index.php?title=svg/attributes/gradientUnits&action=edit&redlink=1) to **userSpaceOnUse** makes the *x*/*y* coordinates correspond to specific points within the graphic:

``` xml
<linearGradient
   id            = "tvOn"
   x1            = "0"
   y1            = "200"
   x2            = "0"
   y2            = "70"
   gradientUnits = "userSpaceOnUse"
>
    <stop  offset="0"    stop-color="#F15A29" />
    <stop  offset="0.05" stop-color="#F15F29" />
    <stop  offset="0.17" stop-color="#F68D24" />
    <stop  offset="0.32" stop-color="#F9AC1C" />
    <stop  offset="0.42" stop-color="#FCBF13" />
    <stop  offset="0.5"  stop-color="#FDC70C" />
    <stop  offset="1"    stop-color="#1C75BC" />
</linearGradient>
```

 ![svg gfx gradient linear.png](//static.webplatform.org/thumb/b/b9/svg_gfx_gradient_linear.png/200px-svg_gfx_gradient_linear.png)

Radial gradients emanate outwards from the center point by default, filling rectangular shapes elliptically. In this example, which generates an obscure cultural reference to an Iggy Pop song, the black color defined at the 30% mark is extrapolated towards the center at 0%:

``` xml
<radialGradient id="tvEye">
  <stop offset="30%"  stop-color="black"     />
  <stop offset="32%"  stop-color="lightblue" />
  <stop offset="58%"  stop-color="lightblue" />
  <stop offset="60%"  stop-color="white"     />
  <stop offset="80%"  stop-color="white"     />
  <stop offset="100%" stop-color="pink"      />
</radialGradient>
```

 ![svg gfx gradient radial.png](//static.webplatform.org/thumb/b/b9/svg_gfx_gradient_radial.png/200px-svg_gfx_gradient_radial.png)

The [**fx**](/w/index.php?title=svg/attributes/fx&action=edit&redlink=1) and [**fy**](/w/index.php?title=svg/attributes/fy&action=edit&redlink=1) attributes specify coordinates for the *focus* of the gradient, while [**cx**](/w/index.php?title=svg/attributes/cx&action=edit&redlink=1) and [**cy**](/w/index.php?title=svg/attributes/cy&action=edit&redlink=1) set the center of the outermost circle. Modifying the [**r**](/w/index.php?title=svg/attributes/r&action=edit&redlink=1) (radius) effectively resizes the gradient, in this case magnifying it relative to the default 0.5 value:

``` xml
<radialGradient id="tvRadial" cx="0.5" cy="0.5" fx="0.8" fy="0.5" r="0.6">
```

 ![svg gfx gradient radialY.png](//static.webplatform.org/thumb/a/a5/svg_gfx_gradient_radialY.png/200px-svg_gfx_gradient_radialY.png)

[View the SVG file here](http://letmespellitoutforyou.com/samples/svg/tv_gradient.svg).

## Patterns

SVG's patterns are similar to CSS's repeating background images, but allow you more control over padding and reorienting patterns. To implement a pattern, you must first design a graphic. In this case, a rectangle fits within a 5×10 area along with a margin of 1 unit:

``` xml
<rect id="tileRect" x="0.5" y="0.5" width="9.0" height="4.0" fill="#E1BC9B" />
```

 ![svg gfx tileRect.png](//static.webplatform.org/thumb/3/35/svg_gfx_tileRect.png/100px-svg_gfx_tileRect.png)

The graphic is wrapped within a [**pattern**](/svg/elements/pattern) element. Its [**width**](/w/index.php?title=svg/attributes/width&action=edit&redlink=1) and [**height**](/w/index.php?title=svg/attributes/height&action=edit&redlink=1) correspond to the intended size of tile. The [**x**](/w/index.php?title=svg/attributes/x&action=edit&redlink=1) and [**y**](/w/index.php?title=svg/attributes/y&action=edit&redlink=1) simply specify the pattern's offset starting point.

``` xml
<pattern
   id                    = "tilePattern"
   x                     = "0"
   y                     = "0"
   width                 = "10"
   height                = "5"
   patternContentUnits   = "userSpaceOnUse"
   patternUnits          = "userSpaceOnUse"
>
  <use xlink:href="#tileRect" />
</pattern>
```

 The units attributes maintain the same fixed coordinate system as for the overall graphic, so that units are not interpreted as percentages of the filled object's dimensions.

Use the [**fill**](/w/index.php?title=svg/properties/fill&action=edit&redlink=1) property to apply the pattern, in this case to a complex [**path**](/svg/elements/path) shape:

``` xml
<path id="headShape" d="M468.054,306.428c0.118,0.623,0.557,0.974,1.042,1.325 ... "/>

<g id="graphic">
  <use xlink:href="#headShape" fill="url(#tilePattern)" />
  <use xlink:href="#shirtShape" />
</g>
```

 ![svg gfx pattern rect.png](//static.webplatform.org/thumb/4/48/svg_gfx_pattern_rect.png/300px-svg_gfx_pattern_rect.png)

Increasing the pattern's [**width**](/w/index.php?title=svg/attributes/width&action=edit&redlink=1) and [**height**](/w/index.php?title=svg/attributes/height&action=edit&redlink=1) attributes allows you control over the tile's margins:

![svg gfx pattern rect wh.png](//static.webplatform.org/thumb/8/86/svg_gfx_pattern_rect_wh.png/300px-svg_gfx_pattern_rect_wh.png)

## More complex tile patterns

This pattern consists of a very simple shape. You can make the pattern's nested set of graphics as complex and varied as you want, or build larger patterns from smaller components. This example shows how to build series of alternating rotated tiles. First, modify the basic shape to include black around the margin:

``` xml
<g id="tileRect">
  <rect id="tileRectWhite" x="0"   y="0"   width="10"  height="5"   fill="#000000" />
  <rect id="tileRectBlack" x="0.5" y="0.5" width="9.0" height="4.0" fill="#E1BC9B" />
</g>
```

 ![svg gfx tileRectBlack.png](//static.webplatform.org/thumb/f/f7/svg_gfx_tileRectBlack.png/100px-svg_gfx_tileRectBlack.png)

A *tileSquare* object duplicates the underlying graphic and uses a [**transform**](/w/index.php?title=svg/attributes/transform&action=edit&redlink=1) to move it below the original to form a 10×10 square:

``` xml
<g id="tileSquare">
  <use xlink:href="#tileRect" />
  <use xlink:href="#tileRect" transform="translate(0,5)"/>
</g>
```

 ![svg gfx tileSquare.png](//static.webplatform.org/thumb/1/1e/svg_gfx_tileSquare.png/100px-svg_gfx_tileSquare.png)

The square is then repeated four times within a larger 20×20 square:

``` xml
<g id="tilePatternUnit">
  <use xlink:href="#tileSquare" />
  <g id="shiftDown" transform="translate(10,10) rotate(90)">
      <use xlink:href="#tileSquare"/>
  </g>
  <g id="shiftOver" transform="translate(10,10) rotate(-90)">
      <use xlink:href="#tileSquare"/>
  </g>
  <g id="shiftDownAndOver" transform="translate(10,10)">
    <use xlink:href="#tileSquare"/>
  </g>
</g>
```

 ![svg gfx tiles.png](//static.webplatform.org/thumb/5/54/svg_gfx_tiles.png/200px-svg_gfx_tiles.png)

All the tiles except for the first one have transforms that move them to the bottom-right corner of the larger square. The second and third are rotated, pivoting around their top-left corners so that they occupy the other two corners. (Unlike CSS transforms, SVG transforms do not *originate* around the object's center point.) Rotating by only 80 degrees may clarify how the transform works:

![svg gfx tiles rot.png](//static.webplatform.org/thumb/a/a8/svg_gfx_tiles_rot.png/200px-svg_gfx_tiles_rot.png)

To apply the modified fill, reference the more complex object, and increase the pattern's tiling area to accomodate it:

``` xml
<pattern
   id                    = "tilePattern"
   x                     = "0"
   y                     = "0"
   width                 = "20"
   height                = "20"
   patternTransform      = "scale(1)"
   patternContentUnits   = "userSpaceOnUse"
   patternUnits          = "userSpaceOnUse"
>
  <use xlink:href="#tilePatternUnit" />
</pattern>
```

 ![svg gfx pattern.png](//static.webplatform.org/thumb/8/87/svg_gfx_pattern.png/300px-svg_gfx_pattern.png)

If the pattern is not sized appropriately for the shape, you do not have to resize the pattern's dimensions or any of the component tiles. The example above specifies a [**patternTransform**](/w/index.php?title=svg/attributes/patternTransform&action=edit&redlink=1) attribute with a *scale(1)* transform that leaves the size unchanged, but increasing the value to 1.5 magnifies the pattern:

![svg gfx pattern scale.png](//static.webplatform.org/thumb/8/82/svg_gfx_pattern_scale.png/300px-svg_gfx_pattern_scale.png)

Other transforms allow you to reorient and reshape the pattern. In this example, *scale(1.5) skewY(15) rotate(30)* boosts the pattern's size, shears it slightly into a diamond shape, and spins it:

![svg gfx pattern skewrot.png](//static.webplatform.org/thumb/1/1e/svg_gfx_pattern_skewrot.png/300px-svg_gfx_pattern_skewrot.png)

[View the SVG file here](http://letmespellitoutforyou.com/samples/svg/pattern_fill.svg).

## Clipping paths

Patterns are not necessarily for tiny images. By applying generous [**width**](/w/index.php?title=svg/attributes/width&action=edit&redlink=1) and [**height**](/w/index.php?title=svg/attributes/height&action=edit&redlink=1) pattern dimensions, you can also use them to display a single large graphic behind an irregular shape. Another way to do this is to apply a *clipping path*, which renders a graphic only inside the contours of another graphic.

Place a [**clipPath**](/svg/elements/clipPath) element around the shape you want to clip the graphic with, in this case the [**path**](/svg/elements/path) we saw earlier that defines the television screen:

``` xml
<clipPath id="screenClip">
    <use xlink:href="#tvScreen"/>
</clipPath>
```

 When rendering the graphic to clip, use the [**clip-path**](/w/index.php?title=svg/properties/clip-path&action=edit&redlink=1) property to reference the [**clipPath**](/svg/elements/clipPath) element:

``` xml
<use xlink:href="#yeller" clip-path="url(#screenClip)" />
<g id="yeller">
  <use xlink:href="#headShape" fill="url(#tilePattern)" />
  <use xlink:href="#shirtShape" />
</g>
```

 ![svg gfx clip.png](//static.webplatform.org/thumb/3/34/svg_gfx_clip.png/200px-svg_gfx_clip.png)

[View the SVG file here](http://letmespellitoutforyou.com/samples/svg/tv_clip.svg).

## Adding images

While SVG is designed for vector graphics, it can freely incorporate raster graphics via the [**image**](/svg/elements/image) element. Use [**x**](/w/index.php?title=svg/attributes/x&action=edit&redlink=1) and [**y**](/w/index.php?title=svg/attributes/y&action=edit&redlink=1) attributes to position an image. Unlike HTML, you need to specify a [**width**](/w/index.php?title=svg/attributes/width&action=edit&redlink=1) and [**height**](/w/index.php?title=svg/attributes/height&action=edit&redlink=1) for an image to appear:

``` xml
<image x="10" y="10" xlink:href="giraffe.png" width="270" height="297"
       preserveAspectRatio="xMidYMid meet"/>
```

 If the supplied dimensions don't match the underlying data, various [**preserveAspectRatio**](/w/index.php?title=svg/attributes/preserveAspectRatio&action=edit&redlink=1) options affect the image's placement. The **meet** keyword fits the entire image, while **slice** clips it. To position the image, you can specify any combination of *Min*, *Mid*, and *Max*, which in the examples below match for each axis, but which you can mix arbitrarily. For example, **xMidYMin** aligns the image at the top, and centers it horizontally. Here are various ways to place a tall graphic in a wide image container:

    xMinYMin meet

![xMinYMin meet.png](//static.webplatform.org/thumb/a/a6/xMinYMin_meet.png/300px-xMinYMin_meet.png)

    xMidYMid meet

![xMidYMid meet.png](//static.webplatform.org/thumb/f/f6/xMidYMid_meet.png/300px-xMidYMid_meet.png)

    xMaxYMax meet

![xMaxYMax meet.png](//static.webplatform.org/thumb/5/54/xMaxYMax_meet.png/300px-xMaxYMax_meet.png)

    xMinYMin slice

![xMinYMin slice.png](//static.webplatform.org/thumb/d/d1/xMinYMin_slice.png/300px-xMinYMin_slice.png)

    xMidYMid slice

![xMidYMid slice.png](//static.webplatform.org/thumb/a/a4/xMidYMid_slice.png/300px-xMidYMid_slice.png)

    xMaxYMax slice

![xMaxYMax slice.png](//static.webplatform.org/thumb/7/79/xMaxYMax_slice.png/300px-xMaxYMax_slice.png)

Images scale depending on the current [**viewBox**](/w/index.php?title=svg/attributes/viewBox&action=edit&redlink=1). For example, if the SVG importing the image appears within a *viewport* of 500×500 pixels (as specified by its own [**width**](/w/index.php?title=svg/attributes/width&action=edit&redlink=1) and [**height**](/w/index.php?title=svg/attributes/height&action=edit&redlink=1)), but its [**viewBox**](/w/index.php?title=svg/attributes/viewBox&action=edit&redlink=1) attribute specifies **0 0 1000 1000**, then the image appears much smaller.

You can also use the [**image**](/svg/elements/image) element to import SVG graphics:

``` xml
<image xlink:href="face_components.svg#eyes" x="10" y="10" width="300" height="100"/>
```

 ![svg image import svg.png](//static.webplatform.org/9/96/svg_image_import_svg.png)

These externally referenced SVG components may animate, but they do not preserve any interactive features.

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

-   **SVG graphic effects**

-   [SVG grand tour](/svg/tutorials/smarter_svg_overview)

-   [SVG filters](/tutorials/svg_filters)
