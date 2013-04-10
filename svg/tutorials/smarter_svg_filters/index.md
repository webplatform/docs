{{Page_Title|SVG filters}}
{{Flags
|High-level issues=Stub
|Checked_Out=Yes
|Editorial notes=[new content edited offline by Sierra ([[User:Sierra|Sierra]] ([[User talk:Sierra|talk]])); please do not edit]
}}
{{Byline}}
{{Summary_Section|This guide shows you how to build SVG image processing filters to create interesting visual effects. It shows how to apply these effects within an SVG graphic, and how to apply them to HTML content using the [[css/properties/filter|'''filter''']] CSS property.}}
{{Tutorial
|Content=

The power of SVG filters is matched by the depth and complexity of
available options. It takes a good deal of practice to master the many
filter effects that are available to you, but hopefully this will help
you understand what's possible.  It starts by showing how modify color
values in ways that often correspond to built-in CSS filter functions.
Then it shows you how to split and merge independent channels to take
advantage of some of SVG's more unusual filter effects.

==What are filters?==

A filter is a little machine that takes graphic input, changes it in
some way, and causes the output to render differently. Filters contain
one or more component ''filter effect'' elements, some of which do
intuitively obvious things (such as blur the graphic), and some of
which only make sense when combined with other effects.

Filter effects are often chained together so that one effect's output
becomes another effect's input. Filter effects may also operate on
different inputs that are modified independently of each other, then
combined.

While the idea of applying filters to web content originated in SVG,
it has recently been extended to CSS, so it helps to clarify what
''filter'' means in these different contexts.  CSS filters currently
come in two flavors:

* Built-in ''filter functions'' provide a series of fairly standard pre-built image processing effects, such as [[css/functions/blur|'''blur()''']] and [[css/functions/grayscale|'''grayscale()''']]. These CSS functions can be chained together to form larger effects, but each one can be represented as an SVG filter.

* In addition to standard two-dimensional image processing features, CSS ''custom filters'' allow you to warp the surface of an element in three dimensions. Custom filters are also known as ''shaders'', either ''vertex'' shaders to warp the surface, or ''fragment'' shaders to modify its pixels.

This guide does not discuss these more recent CSS custom filters, but
does show you how to customize your own SVG filters for use in HTML.

==Applying a simple filter (feGaussianBlur)==

Start by placing some text within an SVG graphic:

<syntaxhighlight lang="xml">
<text class="blurred" x="30" y="100">An SVG Filter</text>
</syntaxhighlight>

[[Image:svgf_none.png]]

Place a [[svg/elements/filter|'''filter''']] element within the SVG's
[[svg/elements/defs|'''defs''']] region.  Filters contain series of
filter effect elements, all prefixed ''fe''.  In this example, a
[[svg/elements/feGaussianBlur|'''feGaussianBlur''']] element produces
a blurring effect, which matches the effect of the
[[css/functions/blur|'''blur()''']] CSS filter function:

<syntaxhighlight lang="xml">
<filter id="css_blur">
  <feGaussianBlur stdDeviation="10"/>
</filter>
</syntaxhighlight>

To apply the filter, reference it with the
[[svg/properties/filter|'''filter''']] property, expressed either as
an attribute or via CSS:

<syntaxhighlight lang="xml" highlight="3">
<text 
  class  = "blurred" 
  filter = "url(#css_blur)" 
  x      = "30" 
  y      = "100"
>An SVG Filter</text>
</syntaxhighlight>

<syntaxhighlight lang="css" highlight="2">
.blurred {
    filter      : url(#blur);
    font-family : sans-serif;
    font-size   : 70px;
    fill        : red;
}
</syntaxhighlight>

[[Image:svgf_blurBoth.png]]

The effect takes each pixel and moves it around randomly from its
original location by a radius specified by the '''stdDeviation'''
value.  Unlike the built-in CSS function, in SVG you can specify
separate ''x'' and ''y'' values to produce a sideways motion effect
that in this case is a bit more legible:

<syntaxhighlight lang="xml">
<filter id="sideways_blur">
  <feGaussianBlur stdDeviation="10 1"/>
</filter>
</syntaxhighlight>

[[Image:svgf_blur.png]]

===Applying SVG filters to HTML===

If you want to apply this customized SVG filter to HTML content, place
it in an SVG file and use the corresponding
[[css/properties/filter|'''filter''']] CSS property to reference it
using the same [[css/functions/url|'''url()''']] function:

<syntaxhighlight lang="css">
.sidewaysBlur {
    -webkit-filter : url(filters.svg#sideways_blur);
    filter         : url(filters.svg#sideways_blur); /* standard in Mozilla */
}
</syntaxhighlight>

As of this writing, not all browsers allow you to apply SVG filters to
HTML content. Mozilla Firefox fully supports the feature.  WebKit
Safari's support is limited to filters that use basic image processing
effects described below: '''feComponentTransfer''',
'''feColorMatrix''', and '''feConvolveMatrix'''.

==Modifying colors with feComponentTransfer==

The [[svg/elements/feComponentTransfer|'''feComponentTransfer''']]
element allows you to modify each RGBA ''component'' represented in
each pixel. Within the element, nest any combination of
[[svg/elements/feFuncR|'''feFuncR''']],
[[svg/elements/feFuncG|'''feFuncG''']],
[[svg/elements/feFuncB|'''feFuncB''']], and
[[svg/elements/feFuncA|'''feFuncA''']] elements to run different types
of function over each pixel component value. 

Setting the [[svg/attributes/type|'''type''']] of function to
'''identity''' is equivalent to leaving out the function element
altogether, keeping the image on the left unchanged.  Setting it to
'''discrete''' allows you to posterize an image, clustering gradual
color shifts into solid bands based on the step values specified in
[[svg/attributes/tableValues|'''tableValues''']]:

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="no_op">
<feComponentTransfer>
  <feFuncR type="identity"/>
  <feFuncG type="identity"/>
  <feFuncB type="identity"/>
  <feFuncA type="identity"/>
</feComponentTransfer>
</filter>
</syntaxhighlight>

[[Image:svgf_CTnoop.png|400px]]

</div>

<div style="display:inline-block">

<syntaxhighlight lang="xml">
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
</syntaxhighlight>

[[Image:svgf_CTband.png|400px]]

</div>

Setting the [[svg/attributes/type|'''type''']] to '''linear'''
multiples the value [[svg/attributes/slope|'''slope''']] value
(relative to the default '''1'''), then adding an
[[svg/attributes/intercept|'''intercept''']] value if present.

The first example reproduces the effect of the CSS
[[css/functions/brightness|'''brightness()''']] function, flattening
the slope to darken the image. The second increases the slope to
brighten the image, but then drops all values by a fixed amount,
zeroing out many of them:

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="css_brightness">
<feComponentTransfer>
 <feFuncR type="linear" slope="0.5"/>
 <feFuncG type="linear" slope="0.5"/>
 <feFuncB type="linear" slope="0.5"/>
</feComponentTransfer>
</filter>
</syntaxhighlight>

[[Image:svgf_CTlinear.png|400px]]

</div>

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="thresholded_brightness">
<feComponentTransfer>
 <feFuncR type="linear" slope="1.5" intercept="-0.3"/>
 <feFuncG type="linear" slope="1.5" intercept="-0.3"/>
 <feFuncB type="linear" slope="1.5" intercept="-0.3"/>
</feComponentTransfer>
</filter>
</syntaxhighlight>

[[Image:svgf_CTlinearIntercept.png|400px]]

</div>

Setting the [[svg/attributes/type|'''type''']] to '''table''' lets you
specify your own linear slope based on two
[[svg/attributes/tableValues|'''tableValues''']].  The first example
behaves like the CSS [[css/functions/opacity|'''opacity()''']]
function.  The second, specifying a negative slope from 1 to 0,
behaves like the CSS [[css/functions/invert|'''invert()''']] function:

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="css_opacity">
<feComponentTransfer>
<feFuncA type="table" tableValues="0 0.5"/>
</feComponentTransfer>
</filter>
</syntaxhighlight>

[[Image:svgf_CTopacity.png|400px]]

</div>

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="css_invert">
<feComponentTransfer>
  <feFuncR type="table" tableValues="1 0"/>
  <feFuncG type="table" tableValues="1 0"/>
  <feFuncB type="table" tableValues="1 0"/>
</feComponentTransfer>
</filter>
</syntaxhighlight>

[[Image:svgf_CTinvert.png|400px]]

</div>

Setting the [[svg/attributes/type|'''type''']] to '''gamma''' allows
you to perform ''gamma correction'', typically to bring up dark
values. The function applies the following formula to produce a curve:
((''amplitude'' &times; ''value''<sup>''exponent''</sup>) +
''offset''). The first example brightens the green, and the second
uses [[svg/attributes/offset|'''offset''']] to reduce the final result
across the board (the same that
[[svg/attributes/intercept|'''intercept''']] does for the '''linear'''
type):

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="gamma_correct">
<feComponentTransfer>
 <feFuncG type="gamma" amplitude="1" exponent="0.5"/>
</feComponentTransfer>
</filter>
</syntaxhighlight>

[[Image:svgf_CTgammaOffset0.png|400px]]

</div>

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="gamma_correct2">
<feComponentTransfer>
 <feFuncG type="gamma" amplitude="1" exponent="0.5"
          offset="-0.1"/>
</feComponentTransfer>
</filter>
</syntaxhighlight>

[[Image:svgf_CTgamma.png|400px]]

</div>

==Transforming colors with feColorMatrix==

The [[svg/elements/feColorMatrix|'''feColorMatrix''']] element provides
other useful ways to modify an image's color. With its
[[svg/attributes/type|'''type''']] set to '''saturate''', reducing the
[[svg/attributes/values|'''values''']] from 1 produces a grayscale,
while increasing it makes the image more vivid, just like the
[[css/functions/grayscale|'''grayscale()''']] and
[[css/functions/saturate|'''saturate()''']] CSS functions:

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="css_grayscale">
  <feColorMatrix type="saturate" values="0"/>
</filter>
</syntaxhighlight>

[[Image:svgf_CMXsaturate0.png|400px]]

</div>

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="css_saturate">
  <feColorMatrix type="saturate" values="10"/>
</filter>
</syntaxhighlight>

[[Image:svgf_CMXsaturate10.png|400px]]

</div>

Setting the [[svg/attributes/type|'''type''']] to '''hueRotate'''
alters the angle along the color wheel, just like the
[[css/functions/hue-rotate|'''hue-rotate()''']] CSS function.  Setting
'''luminanceToAlpha''' (no '''values''' necessary) produces an alpha
channel from bright pixels, useful to produce image masks as described
below.

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="css_hue_rotate">
  <feColorMatrix type="hueRotate" values="180"/>
</filter>
</syntaxhighlight>

[[Image:svgf_CMXhurRotate180.png|400px]]

</div>

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="luminance_mask">
  <feColorMatrix type="luminanceToAlpha"/>
</filter>
</syntaxhighlight>

[[Image:svgf_CMXluminanceToAlpha.png|400px]]

</div>

As the name of the [[svg/elements/feColorMatrix|'''feColorMatrix''']]
suggests, setting the [[svg/attributes/type|'''type''']] to
'''matrix''' allows you to transform colors yourself. It specifies a
20-element transform whose rows correspond to red, green, blue, and
alpha channels. This initial transform leaves the image unchanged:

<div style="display:inline-block">
 1 0 0 0 0
 0 1 0 0 0
 0 0 1 0 0
 0 0 0 1 0  
</div>

The first example below reproduces the effect of the CSS
[[css/functions/sepia|'''sepia()''']] function, while the second
simply reduces green and blue tones. (In these examples, the
[[svg/attributes/values|'''values''']] appear stacked into a table
only in the interest of clarity.)

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="css_sepia">
  <feColorMatrix 
    type="matrix" 
    values=".343 .669 .119 0 0 
            .249 .626 .130 0 0
            .172 .334 .111 0 0
            .000 .000 .000 1 0 "/>
</filter>
</syntaxhighlight>

[[Image:svgf_CMXsepia.png|400px]]

</div>

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<filter id="dusk">
  <feColorMatrix 
    type="matrix" 
    values="1.0 0   0   0   0
            0   0.2 0   0   0 
            0   0   0.2 0   0 
            0   0   0   1.0 0 "/>
</filter>
</syntaxhighlight>

[[Image:svgf_CMXsunset.png|400px]]

</div>

==Sharpening images with feConvolveMatrix==

The [[svg/elements/feConvolveMatrix|'''feConvolveMatrix''']] effect
allows you to modify pixels based on the values of their neighbors,
useful in sharpening details.  In its simplest form, the
[[svg/attributes/order|'''order''']] attribute declares a 3&times;3
box, which defines a matrix of 9 table values that must be reflected
in the [[svg/attributes/kernelMatrix|'''kernelMatrix''']] attribute:

<syntaxhighlight lang="xml">
<filter id="no_op">
  <feConvolveMatrix order="3" kernelMatrix="0 0 0 0 1 0 0 0 0"/>
</filter>
</syntaxhighlight>

The middle value is the pixel to modify, and the others form a map of
its immediate neighbors:

 0 0 0
 0 1 0
 0 0 0

The relative weight of the neighbors helps calculate the pixel's new
value.  In this case it's 0 times each adjacent pixel's value, summed
together along with 1 times the value of the pixel, divided by the sum
of all the pixel values. So this initial example has no effect on the
image.

The original image shown on the left is somewhat blurred.  Applying a
sharpen filter nudges pixels for the higher-contrast edges shown at
the right:

  1  -1  1 
 -1  -1 -1 
  1  -1  1

<div style="display:inline-block">

[[Image:svgf_CVnoop.png|400px]]

</div>

<div style="display:inline-block">

[[Image:svgf_CVsharpen.png|400px]]

</div>

Getting convolve filters to behave predictably takes a bit of
practice.  The example on the left sharpens the detail more
dramatically, while the one on the right embosses it diagonally:

<div style="display:inline-block">

  1  -1    1
 -1  -0.1 -1 
  1  -1    1

[[Image:svgf_CVsuperSharp.png|400px]]

</div>

<div style="display:inline-block">

 9  0  0
 0  1  0
 0  0 -9

[[Image:svgf_CVemboss.png|400px]]

</div>

Convolution filters can also highlight moats around high-contrast
edges.  The more dramatic texture shown below on the right forms moats
throughout the image.  It requires an
[[svg/attributes/order|'''order''']] of 5, which extends the range of
the calculation to each adjacent neighbor's farthest neighbor.  (As
shown here, it is converted to a grayscale using the
'''luminanceToAlpha'''
[[svg/elements/feColorMatrix|'''feColorMatrix''']] type discussed
above, and the effect-chaining technique described below.)

<div style="display:inline-block">

 -1 -1 -1
 -1  7 -1
 -1 -1 -1

[[Image:svgf_CVedge.png|400px]]

</div>

<div style="display:inline-block">

 1   1   1   1  1 
 1  -2  -2  -2  1 
 1  -2  .01 -2  1 
 1  -2  -2  -2  1 
 1   1   1   1  1

[[Image:svgf_CVsuperEdge.png|400px]]

</div>

==Chaining, splitting and merging effects: building a drop shadow with feOffset, feFlood, and feMerge==

Much of the power of SVG filters comes from their ability to accept
various graphic inputs, modify them independently of each other, then
recombine them. This example reproduces the effect produced by the CSS
[[css/functions/drop-shadow|'''drop-shadow()''']] function. Stepping
through each line and seeing the results as you go helps you to build
far more interesting filters:

<syntaxhighlight lang="xml">
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
</syntaxhighlight>

<div style="display:inline-block;max-width:280px;padding:12px">

First we start with an image transparency:

[[Image:svgf_dropNoop.png|192px]]

</div><div style="display:inline-block;max-width:280px;padding:12px">

We've already seen the
[[svg/elements/feGaussianBlur|'''feGaussianBlur''']] effect in action,
but in this case it behaves differently.  The optional
[[svg/attributes/in|'''in''']] specifies the '''SourceAlpha''', or all
of its non-transparent pixels. The result of that effect, which is
colored black, is passed to the next
[[svg/elements/feOffset|'''feOffset''']] effect, which simply moves it
down and over:

[[Image:svgf_dropOffsetBlur.png|192px]]

</div><div style="display:inline-block;max-width:280px;padding:12px">

The [[svg/elements/feFlood|'''feFlood''']] effect simply produces a
color, specified by its
[[svg/properties/flood-color|'''flood-color''']] property.  The effect
is independent of the graphic we've produced so far, and doesn't take
any input from the offset effect, so it renders within the filter's
entire region:

[[Image:svgf_dropFlood.png|192px]]

</div><div style="display:inline-block;max-width:280px;padding:12px">

By default, the [[svg/attributes/result|'''result''']] of the flood
becomes the next effect's [[svg/attributes/in|'''in''']] value, so
neither of these attributes needs to be explicitly declared here.  The
[[svg/elements/feComposite|'''feComposite''']] effect applies the
'''in''' composite operation on the portion of the gray fill that
falls within the dropped shadow:

[[Image:svgf_dropComposite.png|192px]]

</div><div style="display:inline-block;max-width:280px;padding:12px">

Finally, the [[svg/elements/feMerge|'''feMerge''']] effect combines
the modified version of the graphic with the the original. The first
[[svg/elements/feMergeNode|'''feMergeNode''']] accepts the composite
result by default, and the second specifies the '''SourceGraphic''',
which renders over it for the final effect:

[[Image:svgf_dropMerge.png|192px]]

</div>

==Other input and merging options: feBlend, feComposite, feImage, feTile==

The [[svg/elements/feMerge|'''feMerge''']] element shown above simply
places one graphic over another to produce a new filter channel. As an
alternative, you can use [[svg/elements/feBlend|'''feBlend''']] with
its [[svg/attributes/mode|'''mode''']] set to '''normal''', which
combines the [[svg/attributes/in|'''in''']] and
[[svg/attributes/in2|'''in2''']] channels:

<syntaxhighlight lang="xml">
<feBlend in="SourceGraphic" in2="offsetBlur" mode="normal" />
</syntaxhighlight>

The following shows how [[svg/elements/feBlend|'''feBlend''']]'s other
modes affect graphics that overlay each other. The '''lighten''' and
'''darken''' modes simply take the lighter or darker of the two
pixels:

<div style="display:inline-block;max-width:200px;padding:10px">

'''normal'''

[[Image:svgf_blendNormal.png|150px]]

</div><div style="display:inline-block;max-width:200px;padding:10px">

'''lighten'''

[[Image:svgf_blendLighten.png|150px]]

</div><div style="display:inline-block;max-width:200px;padding:10px">

'''darken'''

[[Image:svgf_blendDarken.png|150px]]

</div><div style="display:inline-block;max-width:200px;padding:10px">

'''screen'''

[[Image:svgf_blendScreen.png|150px]]

</div><div style="display:inline-block;max-width:200px;padding:10px">

'''multiply'''

[[Image:svgf_blendMultiply.png|150px]]

</div>

Setting the [[svg/elements/feComposite|'''feComposite''']] element's
[[svg/attributes/operator|'''operator''']] to '''over''' produces the
same default overlay as [[svg/elements/feMerge|'''feMerge''']]:

<syntaxhighlight lang="xml">
<feComposite in="SourceGraphic" in2="offsetBlur" operator="over" />
</syntaxhighlight>

The following shows how its operators behave:

<div style="display:inline-block;max-width:200px;padding:10px">

'''over'''

[[Image:svgf_compOver.png|150px]]

</div><div style="display:inline-block;max-width:200px;padding:10px">

'''out'''

[[Image:svgf_compOut.png|150px]]

</div><div style="display:inline-block;max-width:200px;padding:10px">

'''in'''

[[Image:svgf_compIn.png|150px]]

</div><div style="display:inline-block;max-width:200px;padding:10px">

'''atop'''

[[Image:svgf_compAtop.png|150px]]

</div><div style="display:inline-block;max-width:200px;padding:10px">

'''xor'''

[[Image:svgf_compXor.png|150px]]

</div>

Setting the [[svg/attributes/operator|'''operator''']] to
'''arithmetic''' allows you to supply your own '''k1'''-'''k4''' table
values to produce composite blends.  For example, set
[[svg/attributes/k1|'''k1''']] and [[svg/attributes/k4|'''k4''']] to
0, then decrease [[svg/attributes/k2|'''k2''']] from 1 while
increasing [[svg/attributes/k3|'''k3''']] for a cross-fade effect.
This example makes the [[svg/attributes/in2|'''in2''']] graphic more
visible:

<syntaxhighlight lang="xml">
<feComposite in="graphicA" in2="graphicB" operator="arithmetic" k1="0" k2="0.3" k3="0.7" k4="0"/>
</syntaxhighlight>

[[Image:svgf_compArithmetic.png|150px]]

Use the [[svg/elements/feImage|'''feImage''']] element to import
graphics into filter effects as in the examples above and below. It
allows you to import not only raster images as with the
[[svg/elements/image|'''image''']] element, but any other SVG graphic
as well. By default, graphics are placed in the center of the filter
region.  Otherwise, use [[svg/attributes/x|'''x''']],
[[svg/attributes/y|'''y''']], [[svg/attributes/width|'''width''']],
and [[svg/attributes/height|'''height''']] attributes to reposition
and resize them:

<syntaxhighlight lang="xml">
<feImage xlink:href="img/icon.png" x="100" y="50" width="20%" height="20%" result="icon"/>
<feImage xlink:href="#gradient" result="gradient"/>
<feTile/>
</syntaxhighlight>

The [[svg/elements/feTile|'''feTile''']] element simply allows you to
repeat imported graphics as a pattern.

==Warping effects (feMorphology, feTurbulence, feDisplacementMap)==

The next example shows how to combine several filter effects to warp
text:

<syntaxhighlight lang="xml">
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
</syntaxhighlight>

<div style="display:inline-block;max-width:280px;padding:12px">

Start with a bit of text:

[[Image:svgf_warpStart.png|250px]]

</div><div style="display:inline-block;max-width:280px;padding:12px">

The [[svg/elements/feMorphology|'''feMorphology''']] effect specifies
a [[svg/attributes/dilate|'''dilate''']] factor to thicken the
graphic. (Alternately, [[svg/attributes/erode|'''erode''']] would erode
it.)

[[Image:svgf_warpMorph.png|250px]]

</div><div style="display:inline-block;max-width:280px;padding:12px">

The [[svg/elements/feComponentTransfer|'''feComponentTransfer''']]
modifies the color, as described in a previous section:

[[Image:svgf_warpColoredOutline.png|250px]]

</div><div style="display:inline-block;max-width:280px;padding:12px">

The [[svg/elements/feMerge|'''feMerge''']] places the modified
outline behind the original letterform:

[[Image:svgf_warpCombinedOutline.png|250px]]

</div><div style="display:inline-block;max-width:280px;padding:12px">

The [[svg/elements/feTurbulence|'''feTurbulence''']] effect produces
its own graphic noise within which colors form cloud-like patterns:

[[Image:svgf_warpTurbulence.png|250px]]

</div><div style="display:inline-block;max-width:280px;padding:12px">

The [[svg/elements/feDisplacementMap|'''feDisplacementMap''']]
produces the final effect:

[[Image:svgf_warpDisplace.png|250px]]

</div>

The displacement effect moves the pixels of the text (specified by
[[svg/attributes/in|'''in''']]) based on the pixel values of the noise
pattern (specified by [[svg/attributes/in2|'''in2''']]).  The
[[svg/attributes/xChannelSelector|'''xChannelSelector''']] and
[[svg/attributes/yChannelSelector|'''yChannelSelector''']] specify,
for each axis, which color component's value ('''R''', '''G''',
'''B''', or '''A''') to use to push the pixels, and the
[[svg/attributes/scale|'''scale''']] sets the overall range of
movement.

==Creating textures (feTurbulence)==

Turbulence is indispensible for grain and weave textures, useful for
background patterns.  Step through the following example:

<syntaxhighlight lang="xml">
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
</syntaxhighlight>

<div style="display:inline-block;max-width:200px;padding:12px">

Supplying the [[svg/elements/feTurbulence|'''feTurbulence''']] effect
with two [[svg/attributes/baseFrequency|'''baseFrequency''']] values
creates a striped effect:

[[Image:svgf_TBturb.png|180px]]

</div>

<div style="display:inline-block;max-width:200px;padding:12px">

An [[svg/elements/feComponentTransfer|'''feComponentTransfer''']]
boosts the red values:

[[Image:svgf_TBcomp.png|180px]]

</div>

<div style="display:inline-block;max-width:200px;padding:12px">

An [[svg/elements/feFlood|'''feFlood''']] provides a background color:

[[Image:svgf_TBflood.png|180px]]

</div>

<div style="display:inline-block;max-width:200px;padding:12px">

The final [[svg/elements/feMerge|'''feMerge''']] overlays the pattern:

[[Image:svgf_TBmerge.png|180px]]

</div>

Note the [[svg/elements/filter|'''filter''']] element in the example
above uses [[svg/attributes/x|'''x''']], [[svg/attributes/y|'''y''']],
[[svg/attributes/width|'''width''']], and
[[svg/attributes/height|'''height''']] attributes to specify
dimensions.  By default, filters operate on a ''region'' that's
somewhat wider than elements they are applied to, to account for
offset effects such as the shadow shown above, which extends past the
graphic's original dimensions. In this example, the weave pattern only
appears within the graphic's original dimensions.

<div id="light_effect"></div>

==Lighting effects==

Shining a light on a graphic provides additional depth and texture.
To create a lighting effect, you need to specify three things:

* A light ''color'', specified by the [[svg/properties/lighting-color|'''lighting-color''']] property

* A light ''source'', of which there are three kinds:
** a ''distant'' light ([[svg/elements/feDistantLight|'''feDistantLight''']]) is arbirtarily far away, and so is specified in terms of its angle from the target. This is the most appropriate way to represent sunlight.
** a ''point'' light ([[svg/elements/fePointLight|'''fePointLight''']]) emanates from a specific point that is represented as a three-dimensional ''x''/''y''/''z'' coordinate. This is more appropriate when you need perspective, such as relative to a room light.
** a ''spot'' light ([[svg/elements/feSpotLight|'''feSpotLight''']]) behaves much like a point light, but its beam can be narrowed to a cone, and the light can pivot to other targets.

* A basic ''type'' of light, of which two are available:
** ''diffuse'' light ([[svg/elements/feDiffuseLighting|'''feDiffuseLighting''']]) indicates indirect light from an outside source.
** ''specular'' light ([[svg/elements/feSpecularLighting|'''feSpecularLighting''']]) specifies secondary light that bounced from reflective surfaces.

A graphic's alpha channel forms a ''bump map'' that responds to light.
Transparent values remain flat, while opaque values rise to form peaks
that are illuminated more prominently.  To illustrate how lighting
works, this example generates a hilly terrain:

<syntaxhighlight lang="xml">
<filter id="terrain" x="0" y="0" width="100%" height="100%">
<feTurbulence baseFrequency=".01" numOctaves="2" seed="10" type="turbulence"/>
<feColorMatrix type="luminanceToAlpha"/>
<feComponentTransfer>
 <feFuncA type="table" tableValues="1 0"/>
</feComponentTransfer>
</filter>
</syntaxhighlight>

<div style="display:inline-block;max-width:280px;padding:12px">

The [[svg/elements/feTurbulence|'''feTurbulence''']] provides a noise
pattern.  The darker clusters will become hilltops, and the
surrounding white areas will be valleys:

[[Image:svgf_TERRturb1.png|260px]]

</div><div style="display:inline-block;max-width:280px;padding:12px">

The [[svg/elements/feColorMatrix|'''feColorMatrix''']] element's
'''luminanceToAlpha''' type converts the brighter colors in the
valleys to higher alpha values:

[[Image:svgf_TERRturb2.png|260px]]

</div><div style="display:inline-block;max-width:280px;padding:12px">

The [[svg/elements/feComponentTransfer|'''feComponentTransfer''']]
inverts the alpha channel, so that peaks have higher values and
valleys have lower values:

[[Image:svgf_TERRturb3.png|260px]]

</div>

To specify the lighting effect, nest the light source element
([[svg/elements/feDistantLight|'''feDistantLight''']],
[[svg/elements/fePointLight|'''fePointLight''']],
[[svg/elements/feSpotLight|'''feSpotLight''']]) within the lighting
type ([[svg/elements/feDiffuseLighting|'''feDiffuseLighting''']],
[[svg/elements/feSpecularLighting|'''feSpecularLighting''']]).
This example specifies a distant light:

<syntaxhighlight lang="xml">
<feDiffuseLighting lighting-color="brown" surfaceScale="100" diffuseConstant="1">
  <feDistantLight azimuth="0" elevation="20"/>
</feDiffuseLighting>
</syntaxhighlight>

[[Image:svgf_TERRdiff.png]]

The distant light source's [[svg/attributes/azimuth|'''azimuth''']]
corresponds to a compass angle along the horizon, which lies along the
plane of the display screen.  The
[[svg/attributes/elevation|'''elevation''']] specifies the angle from
the horizon, with 90&deg; facing straight up, or out from the screen.

The diffuse lighting effect's
[[svg/attributes/surfaceScale|'''surfaceScale''']] sets the maximum
height of the hilltops. The
[[svg/attributes/diffuseConstant|'''diffuseConstant''']] sets the
light's saturation, so increasing it from its default value of 1
produces sunlight that's brighter than usual.

The corresponding specular lighting effect only produces highlights,
which can be overlaid on the original scene:

<syntaxhighlight lang="xml">
<feSpecularLighting lighting-color="brown" surfaceScale="100" specularConstant="1">
  <feDistantLight azimuth="0" elevation="20" />
</feSpecularLighting>
</syntaxhighlight>

[[Image:svgf_TERRspec.png]]

This shows the two effects used in combination, with the
[[svg/properties/lighting-color|'''lighting-color''']] property
specified separately in a style sheet. The two lighting effects take
the same ''terrain'' input, then later composite the ''scene'' and its
''highlights'':

<syntaxhighlight lang="css">
.feDiffuseLighting,
.feSpecularLighting {
    lighting-color: brown;
}
</syntaxhighlight>

<syntaxhighlight lang="xml" highlight="4,7,10,13">
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
</syntaxhighlight>

[[Image:svgf_TERRboth.png]]

Setting the filter's
[[svg/attributes/primitiveUnits|'''primitiveUnits''']] to
'''objectBoundingBox''' allows you to specify light sources as
relative percentages, otherwise the default '''userSpaceOnUse''' value
references the coordinate system in effect when the filter was
applied.

A point light allows you to place light sources closer to the scene.
This makes the light appear to hover directly over the graphic:

<syntaxhighlight lang="xml">
<fePointLight x="50%" y="50%" z="200">
</syntaxhighlight>

[[Image:svgf_TERRpoint.png]]

A spot light can direct a beam from the light source to a different
target defined by the [[svg/attributes/pointsAtX|'''pointsAtX''']],
[[svg/attributes/pointsAtY|'''pointsAtY''']], and
[[svg/attributes/pointsAtZ|'''pointsAtZ''']] coordinates.  The
[[svg/attributes/limitingConeAngle|'''limitingConeAngle''']] attribute
allows you to tightly focus the beam:

<syntaxhighlight lang="xml">
<feSpotLight x="0" y="100" z="150" pointsAtX="200" pointsAtY="100" pointsAtZ="0" limitingConeAngle="30"/>
</syntaxhighlight>

[[Image:svgf_TERRspot.png]]

See this
[http://letmespellitoutforyou.com/samples/svg/filter_terrain.svg animated SVG]
that repositions the light sources in these examples.

==Beveling (feSpecularLighting)==

Using lighting effects to bevel graphics adds a greater sense of depth
to the drop-shadow effect seen above.  Step through this example to
build the effect:

<syntaxhighlight lang="xml">
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
</syntaxhighlight>

<div style="display:inline-block;max-width:420px;padding:12px">

Start with some text that appears fairly indistinguishable against a
filled background:

[[Image:svgf_bevelOrig.png]]

</div><div style="display:inline-block;max-width:420px;padding:12px">

The blur pattern is piped to the
[[svg/elements/feOffset|'''feOffset''']] and stored in ''offsetBlur''
for use as the drop shadow. It's also stored in ''blur'' for use by
the lighting effect:

[[Image:svgf_bevelBlur.png]]

</div><div style="display:inline-block;max-width:420px;padding:12px">

The blur not only scatters pixels, but distributes their alpha values
to form a rounded surface, which the lighting effect highlights:

[[Image:svgf_bevelSpec.png]]

</div><div style="display:inline-block;max-width:420px;padding:12px">

The first [[svg/elements/feComposite|'''feComposite''']] clips the
blurred edges that fall outside the graphic's original contours,
available as its '''SourceAlpha''':

[[Image:svgf_bevelCompAlpha.png]]

</div><div style="display:inline-block;max-width:420px;padding:12px">

The second [[svg/elements/feComposite|'''feComposite''']] overlays the
highlight with the original '''SourceGraphic''':

[[Image:svgf_bevelCompImg.png]]

</div><div style="display:inline-block;max-width:420px;padding:12px">

Finally, the ''offsetBlur'' buffer is merged in to provide a drop
shadow for additional depth and legibility:

[[Image:svgf_bevelFinal.png]]

</div>


}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Filters
}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}