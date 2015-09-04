---
title: smarter svg filters
tags:
  - Tutorials
  - SVG
readiness: 'In Progress'
notes:
  - 'Fix multiple broken links'
summary: 'This guide shows you how to build SVG image processing filters to create interesting visual effects. It shows how to apply these effects within an SVG graphic, and how to apply them to HTML content using the filter CSS property.'
uri: 'svg/tutorials/smarter svg filters'
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'tutorials/css filters()'
    - svg/attributes/type
    - svg/attributes/tableValues
    - svg/attributes/slope
    - svg/attributes/intercept
    - svg/attributes/offset
    - svg/attributes/values
    - svg/attributes/order
    - svg/attributes/kernelMatrix
    - svg/attributes/in
    - svg/properties/flood-color
    - svg/attributes/result
    - svg/attributes/mode
    - svg/attributes/in2
    - svg/attributes/operator
    - svg/attributes/k1
    - svg/attributes/k4
    - svg/attributes/k2
    - svg/attributes/k3
    - svg/attributes/x
    - svg/attributes/y
    - svg/attributes/width
    - svg/attributes/height
    - svg/attributes/dilate
    - svg/attributes/erode
    - svg/attributes/xChannelSelector
    - svg/attributes/yChannelSelector
    - svg/attributes/scale
    - svg/attributes/baseFrequency
    - svg/properties/lighting-color
    - svg/elements/feSpotLight
    - svg/attributes/azimuth
    - svg/attributes/elevation
    - svg/attributes/surfaceScale
    - svg/attributes/diffuseConstant
    - svg/attributes/primitiveUnits
    - svg/attributes/pointsAtX
    - svg/attributes/pointsAtY
    - svg/attributes/pointsAtZ
    - svg/attributes/limitingConeAngle

---
# SVG filters

**By Mike Sierra**

## Summary

This guide shows you how to build SVG image processing filters to create interesting visual effects. It shows how to apply these effects within an SVG graphic, and how to apply them to HTML content using the filter CSS property.

The power of SVG filters is matched by the depth and complexity of available options. It takes a good deal of practice to master the many filter effects and understand how to combine them. This guide covers a wide range of examples. It starts by showing how to modify color values in ways that often correspond to built-in CSS filter functions. Then it shows you how to split and merge independent channels to take advantage of some of SVG's more unusual filter effects. Finally, it shows you how to apply three-dimensional lighting effects.

## What are filters?

A filter is a little machine that takes graphic input, changes it in some way, and causes the output to render differently. Filters comprise *filter effect* elements, some of which do intuitively obvious things (such as blur the graphic), and some of which only make sense when combined with other effects. Filter effects are often chained together so that one effect's output becomes another effect's input. Filter effects may also operate on different inputs that are modified independently of each other, then combined.

The idea of applying filters to web content originated in SVG, but it has recently been extended to CSS, so it helps to clarify what *filter* means in that context. CSS filters currently come in two flavors:

-   Built-in *filter functions* provide a series of fairly standard pre-built image processing effects, such as the [**blur()**](/css/functions/blur()) and [**grayscale()**](/css/functions/grayscale()) functions specified by the [**filter**](/css/properties/filter) property. These CSS functions can be chained together to form larger effects. (Each is actually implemented as an SVG filter.) See [Understanding CSS filter effects](/w/index.php?title=tutorials/css_filters()&action=edit&redlink=1) for a guide to these CSS functions.

-   In addition to standard two-dimensional image processing features, CSS *custom filters* allow you to warp the surface of an element in three dimensions using [WebGL](/webgl). Custom CSS filters are also known as *shaders*, either *vertex* shaders that warp a surface, or *fragment* shaders that modify the pixels that cover the resulting surface.

This guide does not discuss these more recent CSS custom filters, but does show you how to customize your own SVG filters for use in HTML.

## Applying a simple filter (feGaussianBlur)

Start by placing some text within an SVG graphic:

``` {.xml}
<text class="blurred" x="30" y="100">An SVG Filter</text>
```

 ![svgf none.png](/assets/public/8/89/svgf_none.png)

Place a [**filter**](/svg/elements/filter) element within the SVG's [**defs**](/svg/elements/defs) region. Filters contain series of filter effect elements, all prefixed *fe*. In this example, a [**feGaussianBlur**](/svg/elements/feGaussianBlur) element produces a blurring effect, which matches the effect of the [**blur()**](/css/functions/blur()) CSS filter function:

``` {.xml}
<filter id="css_blur">
  <feGaussianBlur stdDeviation="10"/>
</filter>
```

 To apply the filter, reference it with the [**filter**](/svg/properties/filter) property, expressed either as an attribute or via CSS:

``` {.xml}
<text
  class  = "blurred"
  filter = "url(#css_blur)"
  x      = "30"
  y      = "100"
>An SVG Filter</text>
```

``` {.css}
.blurred {
    filter      : url(#css_blur);
    font-family : sans-serif;
    font-size   : 70px;
    fill        : red;
}
```

 ![svgf blurBoth.png](/assets/public/2/23/svgf_blurBoth.png)

The effect takes each pixel and moves it around randomly from its original location within a radius specified by the **stdDeviation** value. Unlike the built-in CSS function, in SVG you can specify separate *x* and *y* values to produce a sideways motion effect that in this case is a bit more legible:

``` {.xml}
<filter id="sideways_blur">
  <feGaussianBlur stdDeviation="10 1"/>
</filter>
```

 ![svgf blur.png](/assets/public/a/a9/svgf_blur.png)

### Applying SVG filters to HTML

If you want to apply this customized SVG filter to HTML content, place it in an SVG file and use the corresponding [**filter**](/css/properties/filter) CSS property to reference it using the same [**url()**](/css/functions/url()) function:

``` {.css}
.sidewaysBlur {
    -webkit-filter : url(filters.svg#sideways_blur);
    filter         : url(filters.svg#sideways_blur); /* standard in Mozilla */
}
```

 As of this writing, not all browsers allow you to apply SVG filters to HTML content. Mozilla Firefox fully supports the feature, even allowing filtered elements [to animate](/svg/tutorials/smarter_svg_animation). WebKit Safari's support is limited to filters that use the blur described above, and basic image processing effects described in the first half of this guide: **feComponentTransfer**, **feColorMatrix**, and **feConvolveMatrix**.

## Modifying colors with feComponentTransfer

The [**feComponentTransfer**](/svg/elements/feComponentTransfer) element allows you to modify each RGBA *component* represented in each pixel. Within the element, nest any combination of [**feFuncR**](/svg/elements/feFuncR), [**feFuncG**](/svg/elements/feFuncG), [**feFuncB**](/svg/elements/feFuncB), and [**feFuncA**](/svg/elements/feFuncA) elements to run different types of function over each pixel component value.

Setting the [**type**](/w/index.php?title=svg/attributes/type&action=edit&redlink=1) of function to **identity** is equivalent to leaving out the function element altogether, keeping the image on the left unchanged. Setting it to **discrete** allows you to posterize an image, clustering gradual color shifts into solid bands based on the step values specified in [**tableValues**](/w/index.php?title=svg/attributes/tableValues&action=edit&redlink=1):

``` {.xml}
<filter id="no_op">
<feComponentTransfer>
  <feFuncR type="identity"/>
  <feFuncG type="identity"/>
  <feFuncB type="identity"/>
  <feFuncA type="identity"/>
</feComponentTransfer>
</filter>
```

 ![svgf CTnoop.png](/assets/thumb/7/7e/svgf_CTnoop.png/400px-svgf_CTnoop.png)

``` {.xml}
<filter id="posterize">
  <feComponentTransfer>
    <feFuncR type="discrete"
        tableValues="0 0.2 0.4 0.6 0.8 1"/>
    <feFuncG type="discrete"
        tableValues="0 0.2 0.4 0.6 0.8 1"/>
    <feFuncB type="discrete"
        tableValues="0 0.2 0.4 0.6 0.8 1"/>
  </feComponentTransfer>
</filter>
```

 ![svgf CTband.png](/assets/thumb/2/28/svgf_CTband.png/400px-svgf_CTband.png)

Setting the [**type**](/w/index.php?title=svg/attributes/type&action=edit&redlink=1) to **linear** multiplies the [**slope**](/w/index.php?title=svg/attributes/slope&action=edit&redlink=1) value (relative to the default **1**), then adds an [**intercept**](/w/index.php?title=svg/attributes/intercept&action=edit&redlink=1) value if present. The first example below reproduces the effect of the CSS [**brightness()**](/css/functions/brightness()) function, flattening the slope to darken the image. The second increases the slope to brighten the image, but then drops all values by a fixed amount, zeroing out many of them:

``` {.xml}
<filter id="css_brightness">
<feComponentTransfer>
 <feFuncR type="linear" slope="0.5"/>
 <feFuncG type="linear" slope="0.5"/>
 <feFuncB type="linear" slope="0.5"/>
</feComponentTransfer>
</filter>
```

 ![svgf CTlinear.png](/assets/thumb/8/88/svgf_CTlinear.png/400px-svgf_CTlinear.png)

``` {.xml}
<filter id="brightness_threshold">
<feComponentTransfer>
 <feFuncR type="linear" slope="1.5" intercept="-0.3"/>
 <feFuncG type="linear" slope="1.5" intercept="-0.3"/>
 <feFuncB type="linear" slope="1.5" intercept="-0.3"/>
</feComponentTransfer>
</filter>
```

 ![svgf CTlinearIntercept.png](/assets/thumb/4/4e/svgf_CTlinearIntercept.png/400px-svgf_CTlinearIntercept.png)

Setting the [**type**](/w/index.php?title=svg/attributes/type&action=edit&redlink=1) to **table** lets you specify your own linear slope based on two [**tableValues**](/w/index.php?title=svg/attributes/tableValues&action=edit&redlink=1). The first example behaves like the CSS [**opacity()**](/css/functions/opacity()) function. The second, specifying a negative slope from 1 to 0, behaves like the CSS [**invert()**](/css/functions/invert()) function:

``` {.xml}
<filter id="css_opacity">
<feComponentTransfer>
<feFuncA type="table" tableValues="0 0.5"/>
</feComponentTransfer>
</filter>
```

 ![svgf CTopacity.png](/assets/thumb/b/bd/svgf_CTopacity.png/400px-svgf_CTopacity.png)

``` {.xml}
<filter id="css_invert">
<feComponentTransfer>
  <feFuncR type="table" tableValues="1 0"/>
  <feFuncG type="table" tableValues="1 0"/>
  <feFuncB type="table" tableValues="1 0"/>
</feComponentTransfer>
</filter>
```

 ![svgf CTinvert.png](/assets/thumb/d/d1/svgf_CTinvert.png/400px-svgf_CTinvert.png)

Setting the [**type**](/w/index.php?title=svg/attributes/type&action=edit&redlink=1) to **gamma** allows you to perform *gamma correction*, a useful way to increase dark values. The function applies the following formula to produce a curve: ((*amplitude* × *value*<sup>*exponent*</sup>) + *offset*). The first example heightens the darker greens, and the second uses [**offset**](/w/index.php?title=svg/attributes/offset&action=edit&redlink=1) to reduce the overall green level (the same way that [**intercept**](/w/index.php?title=svg/attributes/intercept&action=edit&redlink=1) does for the **linear** type):

``` {.xml}
<filter id="gamma_correct">
<feComponentTransfer>
 <feFuncG type="gamma" amplitude="1" exponent="0.5"/>
</feComponentTransfer>
</filter>
```

 ![svgf CTgammaOffset0.png](/assets/thumb/4/44/svgf_CTgammaOffset0.png/400px-svgf_CTgammaOffset0.png)

``` {.xml}
<filter id="gamma_correct2">
<feComponentTransfer>
 <feFuncG type="gamma" amplitude="1" exponent="0.5"
          offset="-0.1"/>
</feComponentTransfer>
</filter>
```

 ![svgf CTgamma.png](/assets/thumb/0/04/svgf_CTgamma.png/400px-svgf_CTgamma.png)

## Transforming colors with feColorMatrix

The [**feColorMatrix**](/svg/elements/feColorMatrix) element provides other useful ways to modify an image's color. With its [**type**](/w/index.php?title=svg/attributes/type&action=edit&redlink=1) set to **saturate**, reducing the [**values**](/w/index.php?title=svg/attributes/values&action=edit&redlink=1) from 1 produces a grayscale, while increasing it makes the image more vivid, just like the [**grayscale()**](/css/functions/grayscale()) and [**saturate()**](/css/functions/saturate()) CSS functions:

``` {.xml}
<filter id="css_grayscale">
  <feColorMatrix type="saturate" values="0"/>
</filter>
```

 ![svgf CMXsaturate0.png](/assets/thumb/8/80/svgf_CMXsaturate0.png/400px-svgf_CMXsaturate0.png)

``` {.xml}
<filter id="css_saturate">
  <feColorMatrix type="saturate" values="10"/>
</filter>
```

 ![svgf CMXsaturate10.png](/assets/thumb/8/8b/svgf_CMXsaturate10.png/400px-svgf_CMXsaturate10.png)

Setting the [**type**](/w/index.php?title=svg/attributes/type&action=edit&redlink=1) to **hueRotate** alters the angle along the color wheel, just like the [**hue-rotate()**](/css/functions/hue-rotate()) CSS function. Setting **luminanceToAlpha** (no **values** necessary) produces an alpha channel from bright pixels, useful to produce image masks as described below.

``` {.xml}
<filter id="css_hue_rotate">
  <feColorMatrix type="hueRotate" values="180"/>
</filter>
```

 ![svgf CMXhurRotate180.png](/assets/thumb/6/6d/svgf_CMXhurRotate180.png/400px-svgf_CMXhurRotate180.png)

``` {.xml}
<filter id="luminance_mask">
  <feColorMatrix type="luminanceToAlpha"/>
</filter>
```

 ![svgf CMXluminanceToAlpha.png](/assets/thumb/c/ca/svgf_CMXluminanceToAlpha.png/400px-svgf_CMXluminanceToAlpha.png)

As the name of the [**feColorMatrix**](/svg/elements/feColorMatrix) suggests, setting the [**type**](/w/index.php?title=svg/attributes/type&action=edit&redlink=1) to **matrix** allows you to transform colors yourself. It specifies a 20-element transform whose rows correspond to red, green, blue, and alpha channels. This initial transform leaves the image unchanged:

    1 0 0 0 0
    0 1 0 0 0
    0 0 1 0 0
    0 0 0 1 0

The first example below reproduces the effect of the CSS [**sepia()**](/css/functions/sepia()) function, while the second simply reduces green and blue tones. (In these examples, the [**values**](/w/index.php?title=svg/attributes/values&action=edit&redlink=1) appear stacked into a table only in the interest of clarity.)

``` {.xml}
<filter id="css_sepia">
  <feColorMatrix
    type="matrix"
    values=".343 .669 .119 0 0
            .249 .626 .130 0 0
            .172 .334 .111 0 0
            .000 .000 .000 1 0 "/>
</filter>
```

 ![svgf CMXsepia.png](/assets/thumb/0/02/svgf_CMXsepia.png/400px-svgf_CMXsepia.png)

``` {.xml}
<filter id="dusk">
  <feColorMatrix
    type="matrix"
    values="1.0 0   0   0   0
            0   0.2 0   0   0
            0   0   0.2 0   0
            0   0   0   1.0 0 "/>
</filter>
```

 ![svgf CMXsunset.png](/assets/thumb/7/76/svgf_CMXsunset.png/400px-svgf_CMXsunset.png)

## Sharpening images with feConvolveMatrix

The [**feConvolveMatrix**](/svg/elements/feConvolveMatrix) effect allows you to modify pixels based on the values of their neighbors, useful in sharpening details. In its simplest form, the [**order**](/w/index.php?title=svg/attributes/order&action=edit&redlink=1) attribute declares a 3×3 box, which defines a matrix of 9 table values that must be reflected in the [**kernelMatrix**](/w/index.php?title=svg/attributes/kernelMatrix&action=edit&redlink=1) attribute:

``` {.xml}
<filter id="no_op">
  <feConvolveMatrix order="3" kernelMatrix="0 0 0 0 1 0 0 0 0"/>
</filter>
```

 The middle value is the pixel to modify, and the others form a map of its immediate neighbors:

    0 0 0
    0 1 0
    0 0 0

The relative weight of the neighbors helps calculate the pixel's new value. (In this case it's 0 times each adjacent pixel's value, summed together along with 1 times the value of the pixel, divided by the sum of all the pixel values.) This initial example has no effect on the image.

The original image shown on the left is slightly blurred. Applying a sharpen filter nudges pixels for the higher-contrast edges shown at the right:

     1  -1  1
    -1  -1 -1
     1  -1  1

![svgf CVnoop.png](/assets/thumb/9/9c/svgf_CVnoop.png/400px-svgf_CVnoop.png)

![svgf CVsharpen.png](/assets/thumb/3/34/svgf_CVsharpen.png/400px-svgf_CVsharpen.png)

Getting convolve filters to behave predictably takes a bit of practice. The example on the left below sharpens the detail more dramatically, while the one on the right embosses it diagonally:

     1  -1    1
    -1  -0.1 -1
     1  -1    1

![svgf CVsuperSharp.png](/assets/thumb/9/97/svgf_CVsuperSharp.png/400px-svgf_CVsuperSharp.png)

    9  0  0
    0  1  0
    0  0 -9

![svgf CVemboss.png](/assets/thumb/4/43/svgf_CVemboss.png/400px-svgf_CVemboss.png)

Convolution filters can also highlight moats around high-contrast edges. The more dramatic texture shown below on the right forms moats throughout the image. It requires an [**order**](/w/index.php?title=svg/attributes/order&action=edit&redlink=1) of 5, which extends the range of the calculation to each adjacent neighbor's farthest neighbor.

    -1 -1 -1
    -1  7 -1
    -1 -1 -1

![svgf CVedge.png](/assets/thumb/7/78/svgf_CVedge.png/400px-svgf_CVedge.png)

    1   1   1   1  1
    1  -2  -2  -2  1
    1  -2  .01 -2  1
    1  -2  -2  -2  1
    1   1   1   1  1

![svgf CVsuperEdge.png](/assets/thumb/d/d5/svgf_CVsuperEdge.png/400px-svgf_CVsuperEdge.png)

As shown below, the example on the right is also converted to a grayscale using the **luminanceToAlpha** [**feColorMatrix**](/svg/elements/feColorMatrix) effect described above, and the effect-chaining technique described in the following section.

``` {.xml}
<filter id="extremeEffect">
  <feConvolveMatrix order="5" kernelMatrix="1 1 1 1 1 1 -2 -2 -2 1 1  -2 .01 -2 1 1 -2 -2 -2 1 1 1 1 1 1"/>
  <feColorMatrix type="luminanceToAlpha"/>
</filter>
```

## Chaining, splitting and merging effects: building a drop shadow with feOffset, feFlood, and feMerge

Much of the power of SVG filters comes from their ability to accept various graphic inputs, modify them independently of each other, then recombine them. This example reproduces the effect produced by the CSS [**drop-shadow()**](/css/functions/drop-shadow()) function. Stepping through each line and seeing the results as you go helps you to build far more interesting filters:

``` {.xml}
<filter id="css_drop_shadow">
  <feGaussianBlur stdDeviation="2"  in="SourceAlpha" />
  <feOffset dx="4" dy="6"           result="offsetblur"/>
  <feFlood flood-color="#777"/>
  <feComposite operator="in"        in2="offsetblur"/>
  <feMerge>
    <feMergeNode/>
    <feMergeNode                    in="SourceGraphic"/>
  </feMerge>
</filter>
```

First we start with an image transparency:

![svgf dropNoop.png](/assets/thumb/3/30/svgf_dropNoop.png/192px-svgf_dropNoop.png)

We've already seen the [**feGaussianBlur**](/svg/elements/feGaussianBlur) effect in action, but in this case it behaves differently. The optional [**in**](/w/index.php?title=svg/attributes/in&action=edit&redlink=1) specifies the **SourceAlpha**, or all of its non-transparent pixels. The result of that effect, which is colored black, is passed to the next [**feOffset**](/svg/elements/feOffset) effect, which simply moves it down and over:

![svgf dropOffsetBlur.png](/assets/thumb/0/0c/svgf_dropOffsetBlur.png/192px-svgf_dropOffsetBlur.png)

The [**feFlood**](/svg/elements/feFlood) effect simply produces a color, specified by its [**flood-color**](/w/index.php?title=svg/properties/flood-color&action=edit&redlink=1) property. The effect is independent of the graphic we've produced so far, and doesn't take any input from the offset effect, so it renders within the filter's entire region:

![svgf dropFlood.png](/assets/thumb/6/60/svgf_dropFlood.png/192px-svgf_dropFlood.png)

By default, the [**result**](/w/index.php?title=svg/attributes/result&action=edit&redlink=1) of the flood becomes the next effect's [**in**](/w/index.php?title=svg/attributes/in&action=edit&redlink=1) value, so neither of these attributes needs to be explicitly declared here. The [**feComposite**](/svg/elements/feComposite) effect applies the **in** composite operation on the portion of the gray fill that falls within the dropped shadow:

![svgf dropComposite.png](/assets/thumb/5/59/svgf_dropComposite.png/192px-svgf_dropComposite.png)

Finally, the [**feMerge**](/svg/elements/feMerge) effect combines the modified version of the graphic with the original. The first [**feMergeNode**](/svg/elements/feMergeNode) accepts the composite result by default, and the second specifies the **SourceGraphic**, which renders over it for the final effect:

![svgf dropMerge.png](/assets/thumb/6/6e/svgf_dropMerge.png/192px-svgf_dropMerge.png)

## Other input and merging options: feBlend, feComposite, feImage, feTile

The [**feMerge**](/svg/elements/feMerge) element shown above simply places one graphic over another to produce a new filter channel. As an alternative, you can use [**feBlend**](/svg/elements/feBlend) with its [**mode**](/w/index.php?title=svg/attributes/mode&action=edit&redlink=1) set to **normal**, which combines the [**in**](/w/index.php?title=svg/attributes/in&action=edit&redlink=1) and [**in2**](/w/index.php?title=svg/attributes/in2&action=edit&redlink=1) channels:

``` {.xml}
<feBlend in="SourceGraphic" in2="offsetBlur" mode="normal" />
```

 The following shows how [**feBlend**](/svg/elements/feBlend)'s other modes affect graphics that overlay each other. The **lighten** and **darken** modes simply take the lighter or darker of the two pixels:

**normal**

![svgf blendNormal.png](/assets/thumb/e/e7/svgf_blendNormal.png/150px-svgf_blendNormal.png)

**lighten**

![svgf blendLighten.png](/assets/thumb/a/a2/svgf_blendLighten.png/150px-svgf_blendLighten.png)

**darken**

![svgf blendDarken.png](/assets/thumb/9/93/svgf_blendDarken.png/150px-svgf_blendDarken.png)

**screen**

![svgf blendScreen.png](/assets/thumb/2/2e/svgf_blendScreen.png/150px-svgf_blendScreen.png)

**multiply**

![svgf blendMultiply.png](/assets/thumb/6/6a/svgf_blendMultiply.png/150px-svgf_blendMultiply.png)

Setting the [**feComposite**](/svg/elements/feComposite) element's [**operator**](/w/index.php?title=svg/attributes/operator&action=edit&redlink=1) to **over** produces the same default overlay as [**feMerge**](/svg/elements/feMerge):

``` {.xml}
<feComposite in="SourceGraphic" in2="offsetBlur" operator="over" />
```

 The following shows how its operators behave. The drop-shadow example above uses the **in** operator to fill a color within another graphic.

**over**

![svgf compOver.png](/assets/thumb/6/68/svgf_compOver.png/150px-svgf_compOver.png)

**out**

![svgf compOut.png](/assets/thumb/3/36/svgf_compOut.png/150px-svgf_compOut.png)

**in**

![svgf compIn.png](/assets/thumb/d/d2/svgf_compIn.png/150px-svgf_compIn.png)

**atop**

![svgf compAtop.png](/assets/thumb/c/cb/svgf_compAtop.png/150px-svgf_compAtop.png)

**xor**

![svgf compXor.png](/assets/thumb/0/02/svgf_compXor.png/150px-svgf_compXor.png)

Setting the [**operator**](/w/index.php?title=svg/attributes/operator&action=edit&redlink=1) to **arithmetic** allows you to supply your own **k1**-**k4** table values to produce composite blends. For example, set [**k1**](/w/index.php?title=svg/attributes/k1&action=edit&redlink=1) and [**k4**](/w/index.php?title=svg/attributes/k4&action=edit&redlink=1) to 0, then decrease [**k2**](/w/index.php?title=svg/attributes/k2&action=edit&redlink=1) from 1 while increasing [**k3**](/w/index.php?title=svg/attributes/k3&action=edit&redlink=1) from 0 for a cross-fade effect. This example makes the [**in2**](/w/index.php?title=svg/attributes/in2&action=edit&redlink=1) graphic more visible:

``` {.xml}
<feComposite in="graphicA" in2="graphicB" operator="arithmetic" k1="0" k2="0.3" k3="0.7" k4="0"/>
```

 ![svgf compArithmetic.png](/assets/thumb/0/05/svgf_compArithmetic.png/150px-svgf_compArithmetic.png)

Use the [**feImage**](/svg/elements/feImage) element to import graphics into filter effects as in the examples above and below. It allows you to import not only raster images as with the [**image**](/svg/elements/image) element, but any other SVG graphic as well. By default, graphics are placed in the center of the filter region. Otherwise, use [**x**](/w/index.php?title=svg/attributes/x&action=edit&redlink=1), [**y**](/w/index.php?title=svg/attributes/y&action=edit&redlink=1), [**width**](/w/index.php?title=svg/attributes/width&action=edit&redlink=1), and [**height**](/w/index.php?title=svg/attributes/height&action=edit&redlink=1) attributes to reposition and resize them:

``` {.xml}
<feImage xlink:href="img/icon.png" x="100" y="50" width="20%" height="20%" result="icon"/>
<feImage xlink:href="#gradient" result="gradient"/>
<feTile/>
```

 The [**feTile**](/svg/elements/feTile) element simply allows you to repeat imported graphics as a pattern.

## Warping effects (feMorphology, feTurbulence, feDisplacementMap)

The next example shows how to combine several filter effects to warp text:

``` {.xml}
<filter id="warp" >
  <feMorphology radius="3" operator="dilate"/>
  <feComponentTransfer>
    <feFuncR type="table" tableValues="1 0.5"/>
  </feComponentTransfer>
  <feMerge result="text">
    <feMergeNode/>
    <feMergeNode in="SourceGraphic"/>
  </feMerge>
  <feTurbulence type="fractalNoise" baseFrequency="0.017" numOctaves="1" result="warp" />
  <feDisplacementMap xChannelSelector="R" yChannelSelector="G" scale="60" in="text" in2="warp"  />
</filter>
```

Start with a bit of text:

![svgf warpStart.png](/assets/thumb/d/d2/svgf_warpStart.png/250px-svgf_warpStart.png)

The [**feMorphology**](/svg/elements/feMorphology) effect specifies a [**dilate**](/w/index.php?title=svg/attributes/dilate&action=edit&redlink=1) factor to thicken the graphic. (Alternately, [**erode**](/w/index.php?title=svg/attributes/erode&action=edit&redlink=1) would make it thinner.)

![svgf warpMorph.png](/assets/thumb/4/49/svgf_warpMorph.png/250px-svgf_warpMorph.png)

The [**feComponentTransfer**](/svg/elements/feComponentTransfer) modifies the color, as described in a previous section:

![svgf warpColoredOutline.png](/assets/thumb/b/b7/svgf_warpColoredOutline.png/250px-svgf_warpColoredOutline.png)

The [**feMerge**](/svg/elements/feMerge) places the modified outline behind the original letterform:

![svgf warpCombinedOutline.png](/assets/thumb/c/cd/svgf_warpCombinedOutline.png/250px-svgf_warpCombinedOutline.png)

The [**feTurbulence**](/svg/elements/feTurbulence) effect produces its own graphic noise within which colors form cloud-like patterns:

![svgf warpTurbulence.png](/assets/thumb/2/2b/svgf_warpTurbulence.png/250px-svgf_warpTurbulence.png)

The [**feDisplacementMap**](/svg/elements/feDisplacementMap) produces the final effect:

![svgf warpDisplace.png](/assets/thumb/d/d6/svgf_warpDisplace.png/250px-svgf_warpDisplace.png)

The displacement effect moves the pixels of the text (specified by [**in**](/w/index.php?title=svg/attributes/in&action=edit&redlink=1)) based on the pixel values of the noise pattern (specified by [**in2**](/w/index.php?title=svg/attributes/in2&action=edit&redlink=1)). The [**xChannelSelector**](/w/index.php?title=svg/attributes/xChannelSelector&action=edit&redlink=1) and [**yChannelSelector**](/w/index.php?title=svg/attributes/yChannelSelector&action=edit&redlink=1) specify, for each axis, which color component's value (**R**, **G**, **B**, or **A**) to use to push the pixels, and the [**scale**](/w/index.php?title=svg/attributes/scale&action=edit&redlink=1) sets the overall range of movement.

## Creating textures (feTurbulence)

Turbulence is indispensable for grain and weave textures, useful for background patterns. Step through the following example:

``` {.xml}
<filter id="weave" x="0" y="0" width="100%" height="100%">
 <feTurbulence baseFrequency=".25,.03" numOctaves="3" seed="1"/>
 <feComponentTransfer result="grain">
   <feFuncR type="linear" slope="3"/>
 </feComponentTransfer>
 <feFlood flood-color="brown"/>
 <feMerge>
   <feMergeNode/>
   <feMergeNode in="grain"/>
 </feMerge>
</filter>
```

Supplying the [**feTurbulence**](/svg/elements/feTurbulence) effect with two [**baseFrequency**](/w/index.php?title=svg/attributes/baseFrequency&action=edit&redlink=1) values creates a striped effect:

![svgf TBturb.png](/assets/thumb/a/a5/svgf_TBturb.png/180px-svgf_TBturb.png)

An [**feComponentTransfer**](/svg/elements/feComponentTransfer) boosts the red values:

![svgf TBcomp.png](/assets/thumb/8/8f/svgf_TBcomp.png/180px-svgf_TBcomp.png)

An [**feFlood**](/svg/elements/feFlood) provides a background color:

![svgf TBflood.png](/assets/thumb/0/0d/svgf_TBflood.png/180px-svgf_TBflood.png)

The final [**feMerge**](/svg/elements/feMerge) overlays the pattern:

![svgf TBmerge.png](/assets/thumb/a/a2/svgf_TBmerge.png/180px-svgf_TBmerge.png)

Note the [**filter**](/svg/elements/filter) element in the example above uses [**x**](/w/index.php?title=svg/attributes/x&action=edit&redlink=1), [**y**](/w/index.php?title=svg/attributes/y&action=edit&redlink=1), [**width**](/w/index.php?title=svg/attributes/width&action=edit&redlink=1), and [**height**](/w/index.php?title=svg/attributes/height&action=edit&redlink=1) attributes to specify dimensions. By default, filters operate on a *region* that's somewhat wider than elements they are applied to, to account for offset effects such as the shadow shown above, which extends past the graphic's original dimensions. In this example, the weave pattern only appears within the graphic's original dimensions.

## Lighting effects

Shining a light on a graphic provides additional depth and texture. To create a lighting effect, you need to specify three things:

-   A light *color*, specified by the [**lighting-color**](/w/index.php?title=svg/properties/lighting-color&action=edit&redlink=1) property

-   A light *source*, of which there are three kinds:
    -   a *distant* light ([**feDistantLight**](/svg/elements/feDistantLight)) is arbitrarily far away, and so is specified in terms of its angle from the target. This is the most appropriate way to represent sunlight.
    -   a *point* light ([**fePointLight**](/svg/elements/fePointLight)) emanates from a specific point that is represented as a three-dimensional *x*/*y*/*z* coordinate. This is more appropriate when you need the perspective necessary to place a room light within a scene.
    -   a *spot* light ([**feSpotLight**](/w/index.php?title=svg/elements/feSpotLight&action=edit&redlink=1)) behaves much like a point light, but its beam can be narrowed to a cone, and the light can pivot to other targets.

-   A basic *type* of light, of which two are available:
    -   *diffuse* light ([**feDiffuseLighting**](/svg/elements/feDiffuseLighting)) indicates indirect light from an outside source.
    -   *specular* light ([**feSpecularLighting**](/svg/elements/feSpecularLighting)) specifies secondary light that bounced from reflective surfaces.

A graphic's alpha channel forms a *bump map* that responds to light. Transparent values remain flat, while opaque values rise to form peaks that are illuminated more prominently. To illustrate how lighting works, this example generates a hilly terrain:

``` {.xml}
<filter id="terrain" x="0" y="0" width="100%" height="100%">
<feTurbulence baseFrequency=".01" numOctaves="2" seed="10" type="turbulence"/>
<feColorMatrix type="luminanceToAlpha"/>
<feComponentTransfer>
 <feFuncA type="table" tableValues="1 0"/>
</feComponentTransfer>
</filter>
```

The [**feTurbulence**](/svg/elements/feTurbulence) provides a noise pattern. The darker clusters will become hilltops, and the surrounding white areas will be valleys:

![svgf TERRturb1.png](/assets/thumb/1/11/svgf_TERRturb1.png/260px-svgf_TERRturb1.png)

The [**feColorMatrix**](/svg/elements/feColorMatrix) element's **luminanceToAlpha** type converts the brighter colors in the valleys to higher alpha values:

![svgf TERRturb2.png](/assets/thumb/2/2c/svgf_TERRturb2.png/260px-svgf_TERRturb2.png)

The [**feComponentTransfer**](/svg/elements/feComponentTransfer) inverts the alpha channel, so that peaks have higher values and valleys have lower values:

![svgf TERRturb3.png](/assets/thumb/1/1c/svgf_TERRturb3.png/260px-svgf_TERRturb3.png)

To specify the lighting effect, nest the light source element ([**feDistantLight**](/svg/elements/feDistantLight), [**fePointLight**](/svg/elements/fePointLight), [**feSpotLight**](/w/index.php?title=svg/elements/feSpotLight&action=edit&redlink=1)) within the lighting type ([**feDiffuseLighting**](/svg/elements/feDiffuseLighting), [**feSpecularLighting**](/svg/elements/feSpecularLighting)). This example specifies a distant light:

``` {.xml}
<feDiffuseLighting lighting-color="brown" surfaceScale="100" diffuseConstant="1">
  <feDistantLight azimuth="0" elevation="20"/>
</feDiffuseLighting>
```

 ![svgf TERRdiff.png](/assets/public/a/a5/svgf_TERRdiff.png)

The distant light source's [**azimuth**](/w/index.php?title=svg/attributes/azimuth&action=edit&redlink=1) corresponds to a compass angle along the horizon, which lies along the plane of the display screen. The [**elevation**](/w/index.php?title=svg/attributes/elevation&action=edit&redlink=1) specifies the angle from the horizon, with 90° facing straight up, or out from the screen.

The diffuse lighting effect's [**surfaceScale**](/w/index.php?title=svg/attributes/surfaceScale&action=edit&redlink=1) sets the maximum height of the hilltops. The [**diffuseConstant**](/w/index.php?title=svg/attributes/diffuseConstant&action=edit&redlink=1) sets the light's saturation, so increasing it from its default value of 1 produces sunlight that's brighter than usual.

The corresponding specular lighting effect only produces highlights, which can be overlaid on the original scene:

``` {.xml}
<feSpecularLighting lighting-color="brown" surfaceScale="100" specularConstant="1">
  <feDistantLight azimuth="0" elevation="20" />
</feSpecularLighting>
```

 ![svgf TERRspec.png](/assets/public/c/c3/svgf_TERRspec.png)

This shows the two effects used in combination, with the [**lighting-color**](/w/index.php?title=svg/properties/lighting-color&action=edit&redlink=1) property specified separately in a style sheet. The two lighting effects take the same *terrain* input, then later composite the *scene* and its *highlights*:

``` {.css}
.feDiffuseLighting,
.feSpecularLighting {
    lighting-color: brown;
}
```

``` {.xml}
<filter x="0" y="0" width="100%" height="100%" id="shadow_terrain" primitiveUnits="objectBoundingBox">
<feTurbulence baseFrequency=".01" numOctaves="2" seed="1" type="turbulence"/>
<feColorMatrix type="luminanceToAlpha"/>
<feComponentTransfer result="terrain">
 <feFuncA type="table" tableValues="1 0"/>
</feComponentTransfer>
<feDiffuseLighting surfaceScale="100" in="terrain" result="scene">
  <feDistantLight azimuth="0" elevation="20"/>
</feDiffuseLighting>
<feSpecularLighting surfaceScale="100" in="terrain" result="highlights">
  <feDistantLight azimuth="90" elevation="20" />
</feSpecularLighting>
<feComposite in="scene" in2="highlights" operator="xor"/>
</filter>
```

 ![svgf TERRboth.png](/assets/public/c/ca/svgf_TERRboth.png)

Setting the filter's [**primitiveUnits**](/w/index.php?title=svg/attributes/primitiveUnits&action=edit&redlink=1) to **objectBoundingBox** allows you to specify light sources as relative percentages, otherwise the default **userSpaceOnUse** value references the coordinate system in effect when the filter was applied.

A point light allows you to place light sources closer to the scene. Specify a set of 3D coordinates to position the light source:

``` {.xml}
<fePointLight x="50%" y="50%" z="200">
```

 A spot light can direct a beam from the light source to a different target defined by the [**pointsAtX**](/w/index.php?title=svg/attributes/pointsAtX&action=edit&redlink=1), [**pointsAtY**](/w/index.php?title=svg/attributes/pointsAtY&action=edit&redlink=1), and [**pointsAtZ**](/w/index.php?title=svg/attributes/pointsAtZ&action=edit&redlink=1) coordinates. The [**limitingConeAngle**](/w/index.php?title=svg/attributes/limitingConeAngle&action=edit&redlink=1) attribute allows you to tightly focus the beam:

``` {.xml}
<feSpotLight x="0" y="100" z="150" pointsAtX="200" pointsAtY="100" pointsAtZ="0" limitingConeAngle="30"/>
```

 ![svgf TERRspot.png](/assets/public/3/30/svgf_TERRspot.png)

See this [animated SVG](http://letmespellitoutforyou.com/samples/svg/filter_terrain.svg) that repositions the light sources in these examples.

## Beveling (feSpecularLighting)

Using lighting effects to bevel graphics adds a greater sense of depth to the drop-shadow effect seen above. Step through this example to build the effect:

``` {.xml}
<filter id="bevel" filterUnits="userSpaceOnUse">
  <feGaussianBlur in="SourceAlpha" stdDeviation="4" result="blur"/>
  <feOffset in="blur" dx="4" dy="4" result="offsetBlur"/>
  <feSpecularLighting surfaceScale="5" specularConstant=".75"
      specularExponent="20" lighting-color="#bbbbbb" in="blur"
      result="highlight">
    <fePointLight x="-5000" y="-10000" z="20000"/>
  </feSpecularLighting>
  <feComposite in="highlight" in2="SourceAlpha" operator="in" result="highlight"/>
  <feComposite in="SourceGraphic" in2="highlight" operator="arithmetic"
               k1="0" k2="1" k3="1" k4="0" result="highlightText"/>
  <feMerge>
    <feMergeNode in="offsetBlur"/>
    <feMergeNode in="highlightText"/>
  </feMerge>
</filter>
```

Start with some text that appears fairly indistinguishable against a filled background:

![svgf bevelOrig.png](/assets/public/2/2d/svgf_bevelOrig.png)

The blur pattern is piped to the [**feOffset**](/svg/elements/feOffset) and stored in *offsetBlur* for use as the drop shadow. It's also stored in *blur* for use by the lighting effect:

![svgf bevelBlur.png](/assets/public/8/8f/svgf_bevelBlur.png)

The blur not only scatters pixels, but distributes their alpha values to form a rounded surface, which the lighting effect highlights:

![svgf bevelSpec.png](/assets/public/f/f9/svgf_bevelSpec.png)

The first [**feComposite**](/svg/elements/feComposite) clips the blurred edges that fall outside the graphic's original contours, available as its **SourceAlpha**:

![svgf bevelCompAlpha.png](/assets/public/e/e6/svgf_bevelCompAlpha.png)

The second [**feComposite**](/svg/elements/feComposite) overlays the highlight with the original **SourceGraphic**:

![svgf bevelCompImg.png](/assets/public/1/12/svgf_bevelCompImg.png)

Finally, the *offsetBlur* buffer is merged in to provide a drop shadow for additional depth and legibility:

![svgf bevelFinal.png](/assets/public/a/af/svgf_bevelFinal.png)

Use the same technique to add depth to surfaces, such as this example that defines a radial gradient that fades to transparent values:

``` {.xml}
<circle id="cornea" cx="100" cy="100" r="50" fill="url(#corneaSurface)"/>
<radialGradient id="corneaSurface">
  <stop offset="0%"   stop-color="black" stop-opacity="1"/>
  <stop offset="100%" stop-color="black" stop-opacity="0"/>
</radialGradient>
```

 ![svgf eyeCornea.png](/assets/public/5/5c/svgf_eyeCornea.png)

The filter uses [**feImage**](/svg/elements/feImage) to import an graphic filled with the gradient, then shines a narrow spot light on the surface, which results in a subtle rounded highlight:

``` {.xml}
<filter id="corneaShine" primitiveUnits="objectBoundingBox" >
  <feImage xlink:href="#cornea"/>
  <feSpecularLighting lighting-color="white" surfaceScale="170" specularConstant="2" result="shine">
    <feSpotLight x="200" y="-100" z="200" pointsAtX="120" pointsAtY="80" pointsAtZ="50" limitingConeAngle="7"/>
  </feSpecularLighting>
  <feComposite in="shine" in2="SourceGraphic" operator="over"/>
</filter>
```

 ![svgf eyeShine.png](/assets/public/b/ba/svgf_eyeShine.png)

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

-   **SVG filters**

-   [SVG graphic effects](/svg/tutorials/smarter_svg_graphics)

-   [SVG grand tour](/svg/tutorials/smarter_svg_overview)

-   [SVG filters](/tutorials/svg_filters)

### External resources

-   [SVG Essentials: Filters](http://commons.oreilly.com/wiki/index.php/SVG_Essentials/Filters), by J. David Eisenberg
-   [An SVG Primer for Today's Browsers](http://www.w3.org/Graphics/SVG/IG/resources/svgprimer.html#filters), by David Dailey
-   [Scalable Vector Graphics 1.1, Second Edition](http://www.w3.org/TR/SVG/filters.html)
-   [Hands On: SVG Filter Effects](http://ie.microsoft.com/testdrive/graphics/hands-on-css3/hands-on_svg-filter-effects.htm)

