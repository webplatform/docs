{{Page_Title|SVG grand tour}}
{{Flags}}
{{Byline
|Name=Mike Sierra
}}
{{Summary_Section|
This guide shows you how to build a pair of animating eyeballs, providing a comprehensive tour of SVG features detailed in other tutorials. It shows how to maintain a set of reusable graphic components, and provides essential context on SVG transforms and coordinate spaces.}}
{{Tutorial
|Content=SVG is a standard markup format, like HTML and XML, that
renders ''Scalable Vector Graphics'' within web browsers.  ''Vector'' or
''drawing''-style graphics are implemented as pure shapes that render
crisply at any magnification. In contrast, ''raster'' or
''paint''-style images consist of a series of pixels that may not
display well when zoomed at high resolution.  Use SVG if you want to
freely interact with portions of a graphic.  Since SVG renders within
the browser's DOM, each graphic component can be styled through CSS,
manipulated with JavaScript through core APIs, and can appear
comfortably within HTML pages.

This section of the guide shows how SVG is deployed along with other
core web standards, with which you should already be familiar.  It
highlights some notable differences, and provides a quick tour of many
SVG features that are covered in more detail in other sections. It
focuses on the unique way you can build complex interactive graphics
from reusable components, and how to flexibly resize them and place
them within various drawing surfaces.

<div style="float:right;margin:12px">
[[Image:scr_svg_eyes.png]]
</div>

As part of a grand tour to get a feel for SVG markup, you'll stroll
through an example that shows how to build a pair of eyes, and how to
move them around and make them blink.
[http://letmespellitoutforyou.com/samples/svg_eyeball.html View the accompanying live demo here].

==Defining the drawing area==

There are several ways to deploy SVG, with various options outlined in
the section at the bottom of this page. Examples used throughout this
guide feature ''inline'' SVG that's directly embedded within HTML,
which allows you to flexibly apply CSS and JavaScript to both the SVG
graphic and the HTML content. The basic markup looks like this, with
an [[svg/elements/svg|'''svg''']] element encapsulating the graphics:

<syntaxhighlight lang="html5" highlight="8-11">
<!DOCTYPE html>
<html>
<head>
<title>SVG grand tour demo</title>
<link href="css/eyeballs.css" rel="stylesheet" />
</head>
<body>
<svg width="600" height="200">
   <title>eyeballs</title>
   <desc>interactive demo showcasing several SVG features</desc>
</svg>
<script src="js/eyeballs.js"></script>
</body>
</html>
</syntaxhighlight>

You can add [[svg/elements/title|'''title''']] and
[[svg/elements/desc|'''desc''']] elements wherever necessary to
comment your markup.

(See [[svg/tutorials/smarter_svg_deploy|'''SVG deployment''']] for
different ways to render SVG content.)

==The eyeball==

Adding this line within the [[svg/elements/svg|'''svg''']] region
produces a circle. The [[svg/attributes/cx|'''cx''']] and
[[svg/attributes/cy|'''cy''']] attributes position its center point,
and the [[svg/attributes/r|'''r''']] sizes it relative to that point:

<syntaxhighlight lang="xml">
<circle id="eyeball" cx="100" cy="100" r="50"/>
</syntaxhighlight>

[[Image:svgGrandTour_eyeball_circle_black.png|100px]]

By default, it's filled black. Adding a
[[svg/properties/fill|'''fill''']] attribute allows you to color the
background white, and a [[svg/properties/stroke|'''stroke''']]
attribute helps clarify the edge of the shape:

<syntaxhighlight lang="xml">
<circle id="eyeball" cx="100" cy="100" r="50" fill="white" stroke="black"/>
</syntaxhighlight>

[[Image:svgGrandTour_eyeball_circle_white.png|100px]]

To add the iris and pupil, you can add more circles that specify
different fill colors. Declaring the larger circles first prevents
them from obscuring the smaller ones:

<syntaxhighlight lang="xml">
<circle id="eyeball" cx="100" cy="100" r="50" fill="white" stroke="black"/>
<circle id="iris"    cx="100" cy="100" r="25" fill="lightblue"/>
<circle id="pupil"   cx="100" cy="100" r="12" fill="black"/>
</syntaxhighlight>

[[Image:svgGrandTour_eyeball_circles.png|100px]]

(See [[svg/tutorials/smarter_svg_shapes|'''SVG shapes''']] for more
about basic graphic elements such as circles, ellipses, rectangles,
and polygons.)

==Styling via CSS==

In this example, the [[svg/attributes/id|'''id''']],
[[svg/attributes/cx|'''cx''']], [[svg/attributes/cy|'''cy''']], and
[[svg/attributes/r|'''r''']] are all ordinary ''attributes'', while
the [[svg/properties/fill|'''fill''']] and
[[svg/properties/stroke|'''stroke''']] are known as
''presentation attributes''.
These are simply CSS properties that happen to be expressed as
attributes.  Other than the tendency of longer CSS property names to
use ''dashes-between-lowercase-words'' rather than ''camelCase'' for
attribute names, there may be no way to tell the difference by looking
at them.

Many CSS properties such as [[svg/properties/fill|'''fill''']] and
[[svg/properties/stroke|'''stroke''']] apply only to SVG
content. Some, like [[svg/properties/font-size|'''font-size''']],
apply to both SVG and HTML.  Some behave like CSS properties that you
apply to HTML, but are named differently. The
[[svg/properties/fill|'''fill''']] property provides much the same
capabilities in SVG as the
[[css/properties/background-color|'''background-color''']] and
[[css/properties/background-image|'''background-image''']] properties
do for HTML.  Since [[svg/properties/fill|'''fill''']] is a CSS
property, You can also modify it locally via the
[[svg/attributes/style|'''style''']] attribute. Doing so actually
takes precedence over the value of presentation attributes, so this
example changes the eye color to brown:

<syntaxhighlight lang="xml">
<circle id="iris" cx="100" cy="100" r="25" fill="lightblue" style="fill:brown"/>
</syntaxhighlight>

As in HTML, you can consolidate CSS within style sheets to separate it
from markup. Placing this CSS in the ''eyeballs.css'' file referenced
from the HTML applies it to the slightly pared-down SVG markup that
follows:

<syntaxhighlight lang="css">
#eyeball { fill: white; stroke: black }
#iris { fill: lightblue }
#pupil { fill: black }
</syntaxhighlight>
<syntaxhighlight lang="xml">
<circle id="eyeball" cx="100" cy="100" r="50"/>
<circle id="iris"    cx="100" cy="100" r="25"/>
<circle id="pupil"   cx="100" cy="100" r="12"/>
</syntaxhighlight>

As you'll see below, there are some cases where you want to avoid
using style sheets.

(See [[svg/tutorials/smarter_svg_deploy|'''SVG deployment''']] for
different ways to apply CSS.)

==Applying a gradient==

The concentric circles provide a good way to implement the edge of the
iris and pupil, but are not good for the slight bloodshot color
towards the edge of the eye. As an alternative, you can implement the
entire eyeball as a large circle, within which a radial gradient
builds a series of concentric rings:

<syntaxhighlight lang="xml">
<circle id="eyeball" cx="100" cy="100" r="150" fill="url(#eyeballFill)" />

<radialGradient id="eyeballFill">
  <stop id="inner"           offset="12%"  stop-color="black" />
  <stop id="pupil"           offset="15%"  stop-color="lightblue" />
  <stop id="iris"            offset="27%"  stop-color="lightblue" />
  <stop id="white"           offset="30%"  stop-color="white" />
  <stop id="bloodshotExtent" offset="40%"  stop-color="white" />
  <stop id="outer"           offset="100%" stop-color="pink" />
</radialGradient>
</syntaxhighlight>

[[Image:svgGrandTour_eyeball_fill.png|200px]]

The [[svg/elements/circle|'''circle''']] element's
[[svg/properties/fill|'''fill''']] attribute uses CSS's '''url()'''
function to reference the [[svg/attributes/id|'''id''']] of the
[[svg/elements/radialGradient|'''radialGradient''']] element.  Its nested
[[svg/elements/stop|'''stop''']] elements define fairly abrupt gradations
from the center towards the edge&mdash;from black to blue and then to
white&mdash;followed by a more gradual transition to pink around the
edge of the circle.  SVG gradients work similarly to CSS gradients
available for HTML content, but CSS gradients are only available via
the [[css/properties/background-image|'''background-image''']]
property, which doesn't apply to SVG.

(See [[svg/tutorials/smarter_svg_graphics|'''SVG graphics''']] for
details about gradients, and other information on using patterns and
images.)

==Referencing graphics==

This new circle is much larger than the actual eyeball, because we
want to move it around behind a smaller pair of eyelids. (Don't worry
for now that the shape is wider than the drawing area.) Before you
build the eyelids, you should stash away the graphic components you've
already defined. Add a [[svg/elements/defs|'''defs''']] region to the
[[svg/elements/svg|'''svg''']]:

<syntaxhighlight lang="html5" highlight="11-13">
<!DOCTYPE html>
<html>
<head>
<title>SVG grand tour demo</title>
<link href="css/eyeballs.css" rel="stylesheet" />
</head>
<body>
<svg width="600" height="200">
   <title>eyeballs</title>
   <desc>interactive demo showcasing several SVG features</desc>
   <defs>
      <!-- place components here -->
   </defs>
</svg>
<script src="js/eyeballs.js"></script>
</body>
</html>
</syntaxhighlight>

If you move the [[svg/elements/radialGradient|'''radialGradient''']]
within the [[svg/elements/defs|'''defs''']] region, the
[[svg/elements/circle|'''circle''']] still references it as before,
but if you move the [[svg/elements/circle|'''circle''']] there, it
doesn't render.

The SVG [[svg/elements/use|'''use''']] element allows you a way to reuse
graphic components repeatedly, and to place them in differently sized
areas.  After placing the [[svg/elements/circle|'''circle''']] within
the [[svg/elements/defs|'''defs''']] region, pointing to it with a
[[svg/elements/use|'''use''']] element placed outside the
[[svg/elements/defs|'''defs''']] makes it render:

<syntaxhighlight lang="xml">
<use xlink:href="#eyeball"/>
</syntaxhighlight>

The [[svg/elements/use|'''use''']] element can be a bit mystifying at
first.  It's not simply a copy of the object it points to, but a
''deep reference''.  Any changes made to the prototype
[[svg/elements/circle|'''circle''']] or
[[svg/elements/radialGradient|'''radialGradient''']] components
appears dynamically wherever a [[svg/elements/use|'''use''']] element
references them.  Despite this flexibility, you can't redefine any of
the referenced object's attributes. But you can add optional
presentation attributes that aren't already defined there.

Since the [[svg/elements/use|'''use''']] and its target element are
placed in different parts of the document tree, CSS style sheets that
ordinarily apply to the target do not automatically cascade to the
[[svg/elements/use|'''use''']]. However, you can apply CSS separately
to the [[svg/elements/use|'''use''']] element. This example applies
the same style sheet based on the [[svg/attributes/id|'''id''']] of
the target, and the [[svg/attributes/class|'''class''']] of any
[[svg/elements/use|'''use''']] that references it:

<syntaxhighlight lang="xml">
<style>
#eyeball, .eyeball {
    fill: url(#eyeballFill);
}
</style>
<svg width="200" height="200">
<defs>
<circle id="eyeball" cx="100" cy="100" r="150" />
<defs>
<use xlink:href="#eyeball" class="eyeball" id="eyeball_1"/>
</svg>
</syntaxhighlight>

Note that if the targeted [[svg/elements/circle|'''circle''']] were
also to share the same ''eyeball'' class in this example, then the
[[svg/elements/use|'''use''']] element would not have the flexibility to
be able to change it.

Notice as well that the [[svg/elements/use|'''use''']] element needs the
'''xlink''' namespace to qualify the standard
'''href''' attribute, which is also available in HTML
with no namespace qualifier.  This '''xlink:href''' attribute offers a
different way to reference an object than the CSS '''url()''' syntax
you see in the example above.

==The eyelids==

To place the eyeball within eyelids requires a ''clipping path'',
which allows an object to render only when it appears within another
shape. In this case, the ''eyelids'' shape is a free-form
[[svg/elements/path|'''path''']] whose [[svg/attributes/d|'''d''']]
(''definition'') attribute draws two curves that face each other:

<syntaxhighlight lang="xml">
<path id="eyelids" d="M 200,100 Q 100,200 0,100 Q 100,0 200,100" />
</syntaxhighlight>

[[Image:svgGrandTour_eyeball_eyelid.png|200px]]

Each curve's definition includes ''control points'' that influence the
shape of the curve, but that do not themselves render. Starting from
the right corner (''M'' for ''move to''), the first quadratic (''Q'')
curve's control point is placed at the top, and the destination is the
left corner. The second quadratic curve places its control point at
the bottom corner and ends up at the right corner:

[[Image:svgGrandTour_eyeball_ctrl.png|200px]]

To make the shape behave as a clipping path, place a
[[svg/elements/clipPath|'''clipPath''']] element around the
[[svg/elements/path|'''path''']]. You will actually need to use this shape
again, so it is best to [[svg/elements/use|'''use''']] a reference to it:

<syntaxhighlight lang="xml">
<clipPath id="clipEyelid">
    <use xlink:href="#eyelids" class="eyelids" />
</clipPath>
</syntaxhighlight>

Now apply the [[svg/properties/clip-path|'''clip-path''']] property to apply the clipping path to
the eyeball shape. This example shows it assigned separately via CSS:

<syntaxhighlight lang="css">
.eyeball {
    fill       : url(#eyeballFill);
    clip-path  : url(#clipEyelid);
}
</syntaxhighlight>
<syntaxhighlight lang="xml">
<use xlink:href="#eyeball" class="eyeball" />
</syntaxhighlight>

[[Image:svgGrandTour_eyeball_eyelid_clip.png|200px]]

The only problem now is that the eyelid has disappeared. Clipping
paths don't actually render, so we need to point another reference to
it.  The first [[svg/elements/use|'''use''']] below places the eyeball
within the clipping path, and the second produces the path itself. The
third [[svg/elements/use|'''use''']] that appears outside the
[[svg/elements/defs|'''defs''']] renders the entire object:

<syntaxhighlight lang="xml">
<defs>
<g id="eye">
  <use xlink:href="#eyeball" class="eyeball" />
  <use xlink:href="#eyelids" class="eyelids" />
</g>
</defs>
<use xlink:href="#eye" />
</syntaxhighlight>

[[Image:svgGrandTour_eyeball_eyelid_both.png|200px]]

It becomes useful here to ''group'' the two graphic elements, wrapping
a [[svg/elements/g|'''g''']] element around them to consolidate a larger
semantic ''eye'' object. You can reference the grouped object, and you
will see below, move or otherwise transform it as a unit.

(See [[svg/tutorials/smarter_svg_shapes|'''SVG shapes''']] for details
on path commands, and
[[svg/tutorials/smarter_svg_graphics|'''SVG graphics''']] for clipping
paths.)

==The eyelashes==

Drawing the eyelashes along the eyelid requires a bit of creativity.
We need to add a third reference to the eyelid shape.

<syntaxhighlight lang="xml">
<g id="eye">
  <use xlink:href="#eyelids" class="eyelashes" />
  <use xlink:href="#eyelids" class="eyelids"   />
  <use xlink:href="#eyeball" class="eyeball"   />
</g>
</syntaxhighlight>

The ''eyelashes'' class presents the underlying ''eyelids'' shape much
differently:

<syntaxhighlight lang="css">
.eyelashes {
    fill              : none;
    stroke            : #ddd;
    stroke-width      : 40;
    stroke-dasharray  : 1,10;
    stroke-linejoin   : bevel;
}
</syntaxhighlight>

The [[svg/properties/stroke-width|'''stroke-width''']] thickens the
edge so that it extends both inside and outside the shape.  By
default, the ''stroke'' is solid, but you can apply a ''dash'' pattern
to break it into segments.  Setting the
[[svg/properties/stroke-dasharray|'''stroke-dasharray''']] property to
''1,10'' specifies that for every pixel rendered around the edge of
the shape, skip another ten pixels. This has the effect of drawing
individual eyelashes:

[[Image:svgGrandTour_eyeball_eyelashes.png||200px]]

The beveled [[svg/properties/stroke-linejoin|'''stroke-linejoin''']]
property prevents the stroke from rendering too far past the sharp
corner of the eye where the eyelids meet.

(See [[svg/tutorials/smarter_svg_shapes|'''SVG shapes''']] for details
on various stroke properties.)

==Applying eyeliner==

Even after lightening the color of the stroke, the eyelashes appear
way too crisp and thin compared to the eyeball, and could be softened
and thickened up a bit.  SVG ''filters'' provide many image processing
tools that you can mix and match to produce such special visual
effects.

Add a [[svg/elements/filter|'''filter''']] element to the
[[svg/elements/defs|'''defs''']] region. It serves as a wrapper for
various ''filter effect'' components, which by default are applied in
sequence. In this case, the
[[svg/elements/feGaussianBlur|'''feGaussianBlur''']] effect scatters
the pixels around randomly (a bit more vertically than horizontally),
and [[svg/elements/feComponentTransfer|'''feComponentTransfer''']]
darkens the result:

<syntaxhighlight lang="xml">
<filter
    id           = "soften"
    x            = "-20"
    y            = "-20"
    width        = "250"
    height       = "250"
    filterUnits  = "userSpaceOnUse"
>
  <desc>soften eyelid and eyelashes</desc>
  <feGaussianBlur stdDeviation="1 3" />
  <feComponentTransfer>
      <feFuncR type="linear" slope="0.3"/>
      <feFuncG type="linear" slope="0.3"/>
      <feFuncB type="linear" slope="0.3"/>
  </feComponentTransfer>
</filter>
</syntaxhighlight>

Since the eyelid renders horizontally between 0 and 200 pixels, the
eyelashes spill slightly outside the the left edge of the original
drawing area.  The ''filter'' element's
[[svg/attributes/x|'''x''']]/[[svg/attributes/y|'''y''']]/[[svg/attributes/width|'''width''']]/[[svg/attributes/height|'''height''']]
attributes apply the effect to a wider set of dimensions. Setting
[[svg/attributes/filterUnits|'''filterUnits''']] to
'''userSpaceOnUse''' uses the same coordinate system as the shape to
which the filter is applied; otherwise values would be interpreted as
percentages of the object's bounding box.

Use the [[svg/properties/filter|'''filter''']] property to assign the
effect to the shape used to render the eyelids and eyelashes:

<syntaxhighlight lang="css">
#eyelids {
    filter : url(#soften);
}
</syntaxhighlight>

Here is how it appears, first after the blur, then after the
subsequent darkening:

<div style="display:inline-block">
[[Image:svgGrandTour_eyeball_eyelash_filter_blur.png||200px]]
</div>
<div style="display:inline-block">
[[Image:svgGrandTour_eyeball_eyelid_filters.png||200px]]
</div>

(See [[svg/tutorials/smarter_svg_filters|'''SVG filters''']] for
information on various ways to combine SVG's filter effects.)

==Transforms and coordinate spaces==

To finish off the graphic, group another instance of the ''eye''
object into a higher-level ''eyes'' object:

<syntaxhighlight lang="xml">
<g id="eyes">
  <use xlink:href="#eye"/>
  <use xlink:href="#eye"/>
</g>
</syntaxhighlight>

This renders the same shape twice at the same location. To space them
out, apply a [[svg/attributes/transform|'''transform''']]. This moves
the character's right eye to the right a bit, and the left eye 300
units further:

<syntaxhighlight lang="xml">
<g id="eyes">
  <use xlink:href="#eye" id="eyeRight" transform="translate(50,0)"/>
  <use xlink:href="#eye" id="eyeLeft"  transform="translate(350,0)"/>
</g>
</syntaxhighlight>

The [[svg/attributes/transform|'''transform''']] attribute's
'''translate()''' function provides a flexible way to reposition
objects referenced via [[svg/elements/use|'''use''']], but transforms
can be applied to most any graphic element.  SVG transforms provide
the same functionality as two-dimensional CSS transforms.  The
'''scale()''' function accepts a decimal value to size the object,
where ''1'' is the current size, ''0'' vanishes to a point, and values
greater than 1 increase the size.  The '''rotate()''' function accepts
a ''deg'' or ''rad'' angle measurement that spins the object.  The
'''skewX()''' and '''skewY()''' also accepts an angle with which to
shear the object horizontally or vertically. And '''translate()'''
shifts the object's position.

Once the eyes are semantically grouped, a single
[[svg/elements/use|'''use''']] element outside the
[[svg/elements/defs|'''defs''']] region renders them:

<syntaxhighlight lang="xml">
<use xlink:href="#eyes"/>
</syntaxhighlight>

[[Image:svgGrandTour_eyeballs.png|500px]]

When presenting the eyes with other interface elements, you may want
to resize them.  The original [[svg/elements/svg|'''svg''']] element
specified that they should appear within a 600&times;200-pixel
rectangle:

<syntaxhighlight lang="xml">
<svg width="600" height="200">
</syntaxhighlight>

[[Image:svgGrandTour_eyeballs_viewport_large.png|600px]]

But what if that's much too big for the context in which they are to
appear?  If you shrink it down, using either
[[svg/attributes/width|'''width''']]/[[svg/attributes/height|'''height''']]
attributes or CSS, its dimensions no longer match the various
measurements specified within the graphic:

<syntaxhighlight lang="xml">
<style>
svg {
    width  : 300px;
    height : 100px;
}
</style>
    <!-- ...or... -->
<svg width="300" height="100">
</syntaxhighlight>

[[Image:svgGrandTour_eyeballs_viewport_small.png|300px]]

The solution is to define a custom box using the
[[svg/attributes/viewBox|'''viewBox''']] attribute.  Doing so declares
a set of abstract units for exclusive use ''within'' the graphic,
which may bear no relation to the outer coordinate space in which the
graphic is presented, to which the SVG's
[[svg/attributes/width|'''width''']] and
[[svg/attributes/height|'''height''']] apply:

<syntaxhighlight lang="xml">
<svg width="300" height="100" viewBox="0 0 600 200">
</syntaxhighlight>

[[Image:svgGrandTour_eyeballs_viewbox.png|300px]]

Adding a
[[svg/attributes/preserveAspectRatio|'''preserveAspectRatio''']]
attribute controls what happens in cases when the shape of the
[[svg/attributes/viewBox|'''viewBox''']] doesn't match the
''viewport'' within which the graphic appears. In this case,
'''xMidYMid''' centers it and shrinks it enough for the entire graphic
to appear:

<syntaxhighlight lang="xml">
<svg width="100" height="100" viewBox="0 0 600 200" preserveAspectRatio="xMidYMid">
</syntaxhighlight>

[[Image:svgGrandTour_eyeballs_viewbox_preserve.png|100px]]

==Glancing==

The only remaining problem is that the graphic doesn't actually ''do''
anything.  We want to make the eyes to ''move''.

In many cases, you can use CSS techniques to animate numeric and color
properties that apply to SVG. For example, here's a way to gradually
change the eye color, by toggling between the gradient color stops'
''blue'' and ''brown'' classes:

<syntaxhighlight lang="css">
 .blue  { stop-color   : lightblue; }
 .brown { stop-color   : brown; }
 stop {
    transition         : all 5s;
    -webkit-transition : all 5s;
    -moz-transition    : all 5s;
 }
</syntaxhighlight>

[[Image:svgGrandTour_eyeballs_brown.png|500px]]

You can't use that familiar approach for SVG attributes.  SVG has its
own mechanism (based on the ''SMIL'' standard) to animate attribute
values. We'll use it to make the eye glance to the side.

First, let's try to move the eye statically using a '''translate()'''
transform described above:

<syntaxhighlight lang="xml">
<circle id="eyeball" cx="100" cy="100" r="50" transform="translate(50,0)"/>
</syntaxhighlight>

[[Image:svgGrandTour_eyeballs_translate50.png|500px]]

That certainly didn't do what we want. It moved the entire eyeball,
including the clipping path behind which it is supposed to render.
Instead, modify the [[svg/attributes/cx|'''cx''']] attribute, which
sets the position of the center of the circle:

<syntaxhighlight lang="xml">
<circle id="eyeball" cx="150" cy="100" r="50"/>
</syntaxhighlight>

[[Image:svgGrandTour_eyeball_glance.png|500px]]

That's much better. Now return the [[svg/attributes/cx|'''cx''']] to
its original value.  To get it to move dynamically, place an
[[svg/elements/animate|'''animate''']] element within the ''eyeball''
object whose attribute you want to modify:

<syntaxhighlight lang="xml" highlight="2-10">
<circle id="eyeball" cx="100" cy="100" r="150" >
    <animate
        id             = "glanceStart"
        attributeType  = "XML"
        attributeName  = "cx"
        begin          = "1s"
        dur            = "0.5s"
        from           = "100"
        to             = "150"
    />
</circle>
</syntaxhighlight>

Let's step through what each attribute does:

* [[svg/attributes/attributeType|'''attributeType''']] clarifies that the value we're manipulating is an ''XML'' attribute, not a ''CSS'' property.

* [[svg/attributes/attributeName|'''attributeName''']] provides the name of the attribute to modify, ''cx'' in this case.

* [[svg/attributes/begin|'''begin''']] specifies a delay after which the animation executes, in this case 1 second. A begin value of ''0s'' animates immediately. (If you leave out this attribute, the animation does not play by default, but you can control it with JavaScript as described below.)

* [[svg/attributes/dur|'''dur''']] specifies the animation's duration, half a second in this case.

* [[svg/attributes/from|'''from''']] and [[svg/attributes/to|'''to''']] provide the values between which the animation should transition. In this case, it moves the eyeball 50 units to the right.

As it appears above, the animation moves the eyes to the right, then
immediately snaps back.  There's an attribute called
[[svg/attributes/fill|'''fill''']], which is unfortunately named the
same as the [[svg/properties/fill|'''fill''']] property that applies
colors and gradients to shapes. Adding a
[[svg/attributes/fill|'''fill''']] attribute here and setting it to
'''freeze''' would keep the eyes looking to the side after the
animation ends.  But instead, we'll add another animation to return
the eyes to their original state:

<syntaxhighlight lang="xml" highlight="3,12,15,17-18">
<circle id="eyeball" cx="100" cy="100" r="150" >
    <animate
        id             = "glanceStart"
        attributeType  = "XML"
        attributeName  = "cx"
        begin          = "1s"
        dur            = "0.5s"
        from           = "100"
        to             = "150"
    />
    <animate
        id             = "glanceEnd"
        attributeType  = "XML"
        attributeName  = "cx"
        begin          = "glanceStart.end"
        dur            = "0.5s"
        from           = "150"
        to             = "100"
    />
</circle>
</syntaxhighlight>

Aside from the inversion of the [[svg/attributes/from|'''from''']] and
[[svg/attributes/to|'''to''']] values, note the ''glanceEnd''
animation's [[svg/attributes/begin|'''begin''']] time is expressed in
terms of whenever the previous ''glanceStart'' animation ends. And
notice that in addition to the '''xlink:href''' and '''url()''' syntax
we've seen used to reference objects, now we see a third form of dot
syntax that references the ''glanceStart'' identifier along with the
value of its [[svg/attributes/end|'''end''']] attribute.

(See [[svg/tutorials/smarter_svg_filters|'''SVG animations''']] for
details.)

==Blinking==

As is true for CSS transitions and animations, you can animate most
any numeric or color value. You can also animate complex series of
coordinates used in [[svg/elements/path|'''path''']] definitions, so
long as the sequence of path commands match so that there are
corresponding sets of points.  This allows the eyes to blink. Add this
to the ''eyelids'' object:

<syntaxhighlight lang="xml" highlight="2-10">
<path id="eyelids" d="M 200,100 Q 100,200 0,100 Q 100,0 200,100">
    <animate
        id            = "blink"
        attributeType = "XML"
        attributeName = "d"
        from          = "M 200,100 Q 100,200 0,100 Q 100,0 200,100"
        to            = "M 200,100 Q 100,100 0,100 Q 100,100 200,100"
        begin         = "4s; 6s; 8s; 9s; 11.5s; 13s"
        dur           = "0.1s"
    />
</path>
</syntaxhighlight>

In this case, the [[svg/attributes/begin|'''begin''']] attribute
specifies half a dozen different values, so the animation executes
several times .  Between the [[svg/attributes/from|'''from''']] and
[[svg/attributes/to|'''to''']] values, the only values that are
modified are the positions of the two control points that affect the
shape of the curve, so the animation behaves like this:

[[Image:svgGrandTour_eyeball_blink.png]]

You can use JavaScript to control these animations more flexibly. To
do so, call the '''beginElement()''' method on the animation object.
This example shifts the ''x''/''y'' coordinates to which the eyes
glance, with an optional duration parameter to regulate the speed:

<syntaxhighlight lang="javascript">
function glanceTo(x,y,dur) {
    dur = (dur || 0.5) + 's'; // assign 3rd param or default
    var toThere = document.querySelector('#glanceStart');
    var andBack = document.querySelector('#glanceEnd');
    toThere.setAttribute("to", x + " " + y);
    andBack.setAttribute("from", x + " " + y);
    toThere.setAttribute("dur", dur);
    andBack.setAttribute("dur", dur);
    toThere.beginElement();
}
</syntaxhighlight>

Calling this function keeps the eyes blinking at random points between
two and five seconds:

<syntaxhighlight lang="javascript">
function blink() {
    var minDelay = 2000;
    var maxExtraDelay = 3000;
    document.querySelector('#blink').beginElement();
    setTimeout(blink, (Math.floor(Math.random() * maxExtraDelay) + minDelay));
}
</syntaxhighlight>

(See [[svg/tutorials/smarter_svg_filters|'''SVG animations''']] for
details.)

==Interactive Zoom==

Suppose you want to click on the graphic to get a closer look at it.
Scaling the eyeball would be difficult, because there are now two of
them, and they would collide with each other.  Instead, you can alter
the dimensions of the current [[svg/attributes/viewBox|'''viewBox''']]
to zoom into the scene.

Links use the same [[svg/elements/a|'''a''']] element as in HTML, but
as usual the '''xlink:href''' attribute needs its namespace qualified,
and it needs to wrap other SVG elements rather than plain text.  This
link encapsulates the wrapper for both eyes, so clicking on either one
activates the link:

<syntaxhighlight lang="xml">
<a xlink:href="#zoomIn">
  <use xlink:href="#eyes"/>
</a>
<view id="zoomIn" viewBox="100 50 100 100" />
</syntaxhighlight>



When linking to an internal [[svg/elements/view|'''view''']] element,
its [[svg/attributes/viewBox|'''viewBox''']] value overrides that of
the [[svg/elements/svg|'''svg''']] of which it is a descendant, thus
zooming the scene:

[[Image:svgGrandTour_eyeball_zoom.png|200px]]

The entire eyeball is active by default, but this can be
configured. In HTML content, the
[[css/properties/pointer-events|'''pointer-events''']] property allows
you to control whether an element's mouse and touch event handlers
execute, useful in layered interfaces. SVG allows you to target the
active area to the '''visibleStroke''' or '''visibleFill''' portion of
a graphic (or '''visiblePainted''' for both). These become active when
a graphic's [[css/properties/visibility|'''visibility''']] is enabled
('''visible'''), and when [[svg/properties/fill|'''fill''']] and
[[svg/properties/stroke|'''stroke''']] values are defined.
(Unlike [[css/properties/visibility|'''visibility:hidden''']], setting
[[css/properties/display|'''display:none''']] entirely suppresses an
element's rendering.)

As in HTML, the [[css/properties/cursor|'''cursor''']] property allows
you to highlight active areas, but unlike HTML, ''any'' graphic
element can be styled separately with the ''':hover''' pseudoclass,
not just links:

<syntaxhighlight lang="css">
#eyelid:hover, .eyelids:hover { cursor: pointer; }
#eyelid, .eyelids { pointer-events: visiblePainted; }
</syntaxhighlight>

==Animated Zoom==

There are two problems with the anchor-zoom navigation described
above. First, it only works within SVG files, not inline SVG within
HTML. Second, it executes abruptly, the same way anchor navigation
scrolls an HTML page.

Both problems can be fixed by overriding the default navigation.
First, define alternate [[svg/elements/view|'''view''']] targets along
with an [[svg/elements/animate|'''animate''']] element to shift
between each target's [[svg/attributes/viewBox|'''viewBox''']].
Setting [[svg/attributes/fill|'''fill''']] to '''freeze''' retains the
zoom level after the animation ends:

<syntaxhighlight lang="xml">
<view id="zoomOut" viewBox="0 0 600 200" />
<view id="zoomIn" viewBox="100 50 100 100" />

<animate
   id            = "zoomNav" 
   attributeType = "XML"
   attributeName = "viewBox" 
   fill          = "freeze" 
   />

<a class="zoom" xlink:href="#zoomIn">
  <use xlink:href="#eyes"/>
</a>
</syntaxhighlight>

This JavaScript calls '''preventDefault()''' to disable default
navigation for ''zoom''-classed links. Instead, it executes the
animation modified based on the target's
[[svg/attributes/viewBox|'''viewBox''']]:

<syntaxhighlight lang="javascript">
var animate, svg; // corresponds to SVG elements
var duration = '3s';

window.onload = function() {
    svg = document.querySelector('svg');
    animate = document.querySelector('#zoomNav');
    animate.setAttribute('dur', duration);
    animate.setAttribute('from', svg.getAttribute('viewBox'));
    animate.setAttribute('to', svg.getAttribute('viewBox'));
    var links = document.querySelectorAll('a.zoom');
    for (var i = 0, l = links.length; i < l; i++) {
        // replace default navigation:
        links[i].setAttribute('onclick', 'event.preventDefault()');
        links[i].addEventListener('click', zoomNav);
    }
};

function zoomNav(e) {
    var hash = e.currentTarget.getAttribute('xlink:href');
    var tgt = document.querySelector(hash);
    // swap to/from values:
    animate.setAttribute('from', animate.getAttribute('to'));
    animate.setAttribute('to', tgt.getAttribute('viewBox'));
    // execute animation:
    animate.beginElement();
    // apply CSS class to help customize display within each zoom level:
    svg.className = hash.replace(/#/,'');
}
</syntaxhighlight>

The last line applies different classes to the
[[svg/elements/svg|'''svg''']] container, which we'll use to customize
display of the text elements described below for different zoom
levels.

==Adding Text==

SVG allows you to mix text with other graphics, but these are simple
lines of text that do not wrap within a box as in HTML.  You
ordinarily use '''x''' and '''y''' coordinate attributes to position
[[svg/elements/text|'''text''']] elements directly within a graphic.
This example relies on SVG's characteristic ability to place text
along a curved path:

[[Image:svgGrandTour_eyeball_textRotate.png|200px]]

The text appears to wrap around a [[svg/elements/circle|'''circle''']]
element, but since circles do not have logical start and end points,
you need to use the [[svg/tutorials/smarter_svg_shapes|rather complex]]
''A'' path command to draw two elliptical arc curves, each facing the
other, originating and terminating at the left edge:

<syntaxhighlight lang="xml">
<path id="irisPath" d="M 60,100 A 40,40 0 0 1 140,100 A 40,40 0 0 1 60,100 "/>
<path id="pupilPath" d="M 78,100 A 22,22 0 0 1 122,100 A 22,22 0 0 1 78,100"/>
</syntaxhighlight>

[[Image:svgGrandTour_eyeball_textPath.png|200px]]

We'll add a reference to a ''labels'' object along with other eyeball
components:

<syntaxhighlight lang="xml">
<g id="eye">
  <use xlink:href="#eyelids" class="eyelashes" />
  <use xlink:href="#eyelids" class="eyelids"   />
  <use xlink:href="#eyeball" class="eyeball"   />
  <use xlink:href="#labels"/>
</g>
</syntaxhighlight>

Its [[svg/elements/textPath|'''textPath''']] diverts a portion of the
[[svg/elements/text|'''text''']] to display along the path:

<syntaxhighlight lang="xml">
<g id="labels">
  <text>
    <textPath xlink:href="#irisPath"> Iris </textPath>
  </text>
  <text>
    <textPath xlink:href="#pupilPath"> Pupil </textPath>
  </text>
</g>
</syntaxhighlight>

[[Image:svgGrandTour_eyeball_text.png|200px]]

Ordinarily, you can increment the
[[svg/elements/textPath|'''textPath''']]'s
[[svg/attributes/startOffset|'''startOffset''']] attribute in
animations to push text along the path. As an alternative in this
case, you can use CSS transforms to rotate the circular object:

<syntaxhighlight lang="css">
#irisPath, #pupilPath {
    fill             : none;
    transform-origin : center         ; -webkit-transform-origin : center  ; -moz-transform-origin : center;
}
#irisPath {
    transform        : rotate(120deg) ; -webkit-transform : rotate(120deg) ; -moz-transform : rotate(120deg);
}
#pupilPath {
    transform        : rotate(20deg)  ; -webkit-transform : rotate(20deg)  ; -moz-transform : rotate(20deg);
}
</syntaxhighlight>

By default, SVG transforms originate from an element's top-left
corner, so to spin the circle properly you need to explicitly set the
[[css/properties/transform-origin|'''transform-origin''']] property to
CSS's own default '''50% 50%''' value. And be careful when mixing
transforms, since SVG's get clobbered by CSS's.

[[Image:svgGrandTour_eyeball_textRotate.png|200px]]

Finally, additional CSS specifies the appearance of the text labels,
and displays contextually within the magnified zoom level. Transitions
on the [[svg/properties/fill-opacity|'''fill-opacity''']] and
[[svg/properties/stroke-opacity|'''stroke-opacity''']] properties fade
them in and out as the zoom animation executes:

<syntaxhighlight lang="css">
text {
    font-size          : 10px;
    text-transform     : uppercase;
    stroke-width       : 0.5;
    stroke             : black;
    stroke-opacity     : 0;
    fill               : red;
    fill-opacity       : 0;
    /* transition to default zoom level lasts 2 seconds; no delay */
    transition         : all 2s;    -webkit-transition : all 2s;    -moz-transition    : all 2s;
}

svg.zoomIn text {
    fill-opacity       : 0.25;
    stroke-opacity     : 0.25;
    /* transition to magnified zoom level lasts 2 seconds, with 2 second delay */
    transition         : all 2s 2s;    -webkit-transition : all 2s 2s;    -moz-transition    : all 2s 2s;
}
</syntaxhighlight>

Text letterforms behave just like paths, so the various and fill and
stroke properties work the same way as for other shapes.

(See [[svg/tutorials/smarter_svg_text|'''SVG text''']] for details on
text properties.)

Had enough?

[[Image:svgGrandTour_eyeball_tired.png|600px]]

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