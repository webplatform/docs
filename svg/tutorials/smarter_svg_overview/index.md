{{Page_Title|SVG: Grand Tour}}
{{Flags
|High-level issues=Stub
|Editorial notes=[new content edited offline by Sierra ([[User:Sierra|Sierra]] ([[User talk:Sierra|talk]])); please do not edit]
}}
{{Byline}}
{{Summary_Section|This guide introduces SVG graphics and shows you all the basics of how to deploy them along with standard web content.}}
{{Tutorial
|Content=SVG is a standard markup format, like HTML and XML, that
renders ''Scalable Vector Graphics'' within web browsers.  Vector or
''drawing''-style graphics are implemented as pure shapes that render
crisply at any magnification. In contrast, ''raster'' or
''paint''-style images consist of a series of pixels that may not
display well when zoomed at high resolution.  Use SVG if you want to
freely interact with portions of a graphic.  Since SVG renders within
the browser's DOM, each graphic component can be styled through CSS,
manipulated with JavaScript through core APIs, and can appear
comfortably alongside HTML content.

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
an '''svg''' tag encapsulating the graphics:

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

You can add '''title''' and '''desc''' tags wherever necessary to
comment your markup.

==The eyeball==

Adding this line within the '''svg''' region produces a circle. The
'''cx''' and '''cy''' attributes position its center point, and the
'''r''' sizes it relative to that point:

<syntaxhighlight lang="xml">
<circle id="eyeball" cx="100" cy="100" r="50"/>
</syntaxhighlight>

[[Image:svgGrandTour_eyeball_circle_black.png|100px]]

By default, it's filled black. Adding a '''fill''' attribute allows
you to color the background white, and a '''stroke''' attribute helps
clarify the edge of the shape:

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

==Styling via CSS==

In this example, the '''id''', '''cx''', '''cy''', and '''r''' are all
ordinary ''attributes'', while the '''fill''' and '''stroke''' are
known as ''presentation attributes''.  These are simply CSS properties
that happen to be expressed as attributes.  Other than the tendency of
longer CSS property names to use ''dashes-between-lowercase-words''
rather than ''camelCase'' for attribute names, there may be no way to
tell the difference by looking at them.

Many CSS properties such as '''fill''' and '''stroke''' apply only to
SVG content. Some, like '''font-size''', apply to both SVG and HTML.
Some behave like CSS properties that you apply to HTML, but are named
differently. The '''fill''' property provides much the same
capabilities in SVG as the '''background-color''' and
'''background-image''' properties do for HTML.  Since '''fill'''
is CSS, You can also modify it locally via the '''style'''
attribute. Doing so actually takes precedence over the value of
presentation attributes, so this example changes the eye color to
brown:

<syntaxhighlight lang="xml">
<circle id="iris" cx="100" cy="100" r="25" fill="lightblue" style="fill:brown"/>
</syntaxhighlight>

As in HTML, you can consolidate CSS in style sheets and separate it
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
using style sheets. The examples below show CSS applied as
presentational attributes.

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

The '''circle''' tag's '''fill''' attribute uses CSS's '''url()'''
function to reference the '''id''' of the '''radialGradient''' tag.
Its nested '''stop''' tags define fairly abrupt gradations from the
center towards the edge&mdash;from black to blue and then to
white&mdash;followed by a more gradual transition to pink around the
edge of the circle.  SVG gradients work similarly to CSS gradients
available for HTML content, but CSS gradients are only available via
the '''background-image''' property, which doesn't apply to SVG.

==Referencing graphics==

This new circle is much larger than the actual eyeball, because we
want to move it around behind a smaller pair of eyelids. (Don't worry
for now that the shape is too wide.) Before you build the eyelids, you
should stash away the graphic components you've already defined. Add a
'''defs''' region to the '''svg''':

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

If you move the '''radialGradient''' within the '''defs''' region, the
'''circle''' still references it as before, but if you move the
'''circle''' there, it doesn't render.

The SVG '''use''' tag allows you a way to reuse graphic components
repeatedly, and to place them in differently sized areas.  After
placing the '''circle''' within the '''defs''' region, pointing to it
with a '''use''' tag placed outside the '''defs''' makes it render:

<syntaxhighlight lang="xml">
<use xlink:href="#eyeball"/>
</syntaxhighlight>

The '''use''' tag can be a bit mystifying at first.  It's not simply a
copy of the object it points to, but a ''deep'' reference.  That means
any changes made to the prototype '''circle''' or '''radialGradient'''
components within the '''defs''' appears dynamically wherever a
'''use''' tag references them.  Despite this flexibility, you can't
redefine any of the referenced object's attributes. But you can add
optional presentation attributes that aren't already defined there.

Since the '''use''' and its target element are placed in different
parts of the document tree, CSS style sheets that ordinarily apply to
the target do not automatically cascade to the '''use'''. However, you
can apply CSS separately to the '''use'''. This example applies the
same style sheet based on the '''id''' of the target, and the
'''class''' of any '''use''' that references it:

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

Note that if the targeted '''circle''' were also to share the same
''eyeball'' class in this example, then the '''use''' tag would not
have the flexibility to be able to change it.

Notice as well that the '''use''' tag needs the '''xlink''' namespace
to qualify the standard '''href''' attribute, which is also available
in HTML with no namespace qualifier.  This '''xlink:href''' attribute
offers a different way to reference an object than the CSS '''url()'''
syntax you see in the example above.

==The eyelids==

To place the eyeball within eyelids requires a ''clipping path'',
which allows an object to render only when it appears within another
shape. In this case, the ''eyelids'' shape is a free-form '''path'''
whose '''d''' (''definition'') attribute draws two curves that face
each other:

<syntaxhighlight lang="xml">
<path
   id = "eyelids"
   d  = "M 200,100 Q 100,200 0,100 Q 100,0 200,100"
   >
</syntaxhighlight>

[[Image:svgGrandTour_eyeball_eyelid.png|200px]]

Each curve's definition includes ''control points'' that influence the
shape of the curve, but that do not themselves render. Starting from
the right corner (''M'' for ''move to''), the first quadratic (''Q'')
curve's control point is placed at the top, and the destination is the
left corner. The second quadratic curve places its control point at
the bottom corner and ends up at the right corner:

[[Image:svgGrandTour_eyeball_ctrl.png|200px]]

To make the shape behave as a clipping path, place a '''clipPath'''
tag around the '''path'''. You will actually need to use this shape
again, so it is best to '''use''' a reference to it:

<syntaxhighlight lang="xml">
<clipPath id="clipEyelid">
    <use xlink:href="#eyelids" class="eyelids" />
</clipPath>
</syntaxhighlight>

Now apply the '''clip-path''' property to apply the clipping path to
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
it.  The first '''use''' below places the eyeball within the clipping
path, and the second produces the path itself. The third '''use'''
that appears outside the '''defs''' renders the entire object:

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
a '''g''' tag around them to consolidate a larger semantic ''eye''
object. In addition to the ability to reference them, you will see
below that you can move them or otherwise transform them as a unit.

==The eyelashes==

Drawing the eyelashes requires a bit of creativity. We need to add yet
another reference to the eyelid shape:

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

The '''stroke-width''' thickens the edge so that it extends both
inside and outside the shape.  By default, the ''stroke'' is solid,
but you can apply a ''dash'' pattern to break it into segments.
Setting the '''stroke-dasharray''' property to ''1,10'' specifies that
for every pixel rendered around the edge of the shape, skip another
ten pixels. This has the effect of drawing individual eyelashes:

[[Image:svgGrandTour_eyeball_eyelashes.png||200px]]

The '''stroke-linejoin''' property prevents the stroke from rendering
too far past the sharp corner of the eye where the eyelids meet.

==Applying eyeliner==

Even after lightening the color of the stroke, the eyelashes appear
way too crisp and detailed compared to the eyeball, and could be
softened up a bit.  SVG ''filters'' provide many image processing
tools that you can mix and match to produce such special visual
effects.

Add a '''filter''' element to the '''defs''' region. It serves as a
wrapper for various ''filter effect'' components, which by default are
applied in sequence. In this case, the '''feGaussianBlur''' effect
scatters the pixels around randomly, and '''feComponentTransfer'''
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
drawing area.  The ''filter'' tag's
'''x'''/'''y'''/'''width'''/'''height''' attributes apply the effect
to a wider set of dimensions. Setting '''filterUnits''' to
'''userSpaceOnUse''' uses the same coordinate system as the shape to
which the filter is applied; otherwise values would be interpreted as
percentages of the object's bounding box.

Use the '''filter''' property to assign the effect to the shape used
to render the eyelids and eyelashes:

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

==Coordinate spaces and transforms==

To finish off the graphic, group another instance of the ''eye''
object into a higher-level ''eyes'' object:

<syntaxhighlight lang="xml">
<g id="eyes">
  <use xlink:href="#eye"/>
  <use xlink:href="#eye"/>
</g>
</syntaxhighlight>

This renders the same shape twice at the same location. To space them
out, apply a '''transform'''. This moves the character's right eye to
the right a bit, and the left eye 300 units further:

<syntaxhighlight lang="xml">
<g id="eyes">
  <use xlink:href="#eye" id="eyeRight" transform="translate(50,0)"/>
  <use xlink:href="#eye" id="eyeLeft"  transform="translate(350,0)"/>
</g>
</syntaxhighlight>

The '''transform''' attribute's '''translate()''' function provides a
flexible way to reposition objects referenced via '''use''', but
transforms can be applied to most any graphic element.  SVG transforms
provide the same functionality as two-dimensional CSS transforms.  The
'''scale()''' function accepts a decimal value to size the object,
where ''1'' is the current size, ''0'' vanishes to a point, and values
greater than 1 increase the size.  The '''rotate()''' function accepts
a ''deg'' or ''rad'' angle measurement that spins the object.  The
'''skewX()''' and '''skewY()''' also accepts an angle with which to
shear the object horizontally or vertically. And '''translate()'''
shifts the object's position.

Once the eyes are semantically grouped, a single '''use''' tag outside
the '''defs''' region renders them:

<syntaxhighlight lang="xml">
<use xlink:href="#eyes"/>
</syntaxhighlight>

[[Image:svgGrandTour_eyeballs.png|500px]]

When presenting the eyes with other interface elements, you may want
to resize them.  The original '''svg''' tag specified that they should
appear within a 600&times;200-pixel rectangle:

<syntaxhighlight lang="xml">
<svg width="600" height="200">
</syntaxhighlight>

[[Image:svgGrandTour_eyeballs_viewport_large.png|600px]]

But what if that's much too big for the context in which they are to
appear?  If you shrink it down, using either the tag's
'''width'''/'''height''' attributes or CSS, its dimensions no longer
match the various measurements specified within the graphic:

<syntaxhighlight lang="xml">
<style>
svg {
    width  : 300;
    height : 100;
}
</style>
    <!-- ...or... -->
<svg width="300" height="100">
</syntaxhighlight>

[[Image:svgGrandTour_eyeballs_viewport_small.png|300px]]

The solution is to define a custom box using the '''viewBox'''
attribute.  Doing so declares a set of abstract units for exclusive
use within the graphic, which may bear no relation to the coordinate
space within which the graphic appears, to which the SVG's '''width'''
and '''height''' apply:

<syntaxhighlight lang="xml">
<svg width="300" height="100" viewBox="0 0 600 200">
</syntaxhighlight>

[[Image:svgGrandTour_eyeballs_viewbox.png|300px]]

Adding a '''preserveAspectRatio''' attribute controls what happens in
cases when the shape of the '''viewBox''' doesn't match the
''viewport'' within which the graphic appears. In this case,
'''xMidYMid''' centers it and shrinks it enough for the entire graphic
to appear:

<syntaxhighlight lang="xml">
<svg width="100" height="100" viewBox="0 0 600 200" preserveAspectRatio="xMidYMid">
</syntaxhighlight>

[[Image:svgGrandTour_eyeballs_viewbox_preserve.png|100px]]

==Blinking and glancing==

The only remaining problem is that the graphic doesn't actually ''do''
anything.  We want to make the eyes to ''move''.

In a few marginal cases, you can use CSS techniques to animate numeric
and color properties that apply to SVG. For example, here's a way to
gradually change the eye color, by toggling between the gradient color
stops' ''blue'' and ''brown'' classes:

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

That didn't do what we want. That moved the entire eyeball, including
the clipping path behind which it is supposed to render. Instead,
modify the '''cx''' attribute, which positions the center of the
circle:

<syntaxhighlight lang="xml">
<circle id="eyeball" cx="150" cy="100" r="50"/>
</syntaxhighlight>

[[Image:svgGrandTour_eyeball_glance.png|500px]]

That's better. Now return the '''cx''' to its original value.  To get
it to move instead, place an '''animate''' tag within the ''eyeball''
object whose attribute you want to modify:

<syntaxhighlight lang="xml" highlight="2-11">
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

Let's run down what each attribute does:

* '''attributeType''' clarifies that the value we're manipulating is an ''XML'' attribute, not a ''CSS'' property.

* '''attributeName''' provides the name of the attribute to modify, ''cx'' in this case.

* '''begin''' specifies a delay after which the animation executes, in this case 1 second. A begin value of ''0s'' animates immediately. (If you leave out this attribute, the animation does not play by default, but you can control it with JavaScript as described below.)

* '''dur''' specifies the animation's duration, half a second in this case.

* '''from''' and '''to''' provide the values between which the animation should transition. In this case, it moves the eyeball 50 units to the right.

As it appears above, the animation moves the eyes to the right, then
immediately snaps back:

[[Image:svgGrandTour_eyeball_glance.png]]

There's an attribute called '''fill''', which is unfortunately named
the same as the '''fill''' property that applies colors and gradients
to shapes. Adding a '''fill''' attribute here and setting it to
'''freeze''' would keep the eyes looking right after the animation
ends.  But instead, we'll add another animation to return the eyes so
that they look ahead:

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

Aside from the values of '''from''' and '''to''' being inverted, note
the '''begin''' time is expressed in terms of whenever the previous
animation ends. And notice that in addition to the '''xlink:href'''
and '''url()''' syntax we've seen used to reference objects, now we
see a third form of ''id.attr'' notation.

As is true for CSS transitions and animations, you can animate most
any numeric or color value. You can also animate complex series of
coordinates used in '''path''' definitions, so long as the sequence of
path commands match so that there are corresponding sets of points.
This allows the eyes to blink. Add this to the ''eyelids'' object:

<syntaxhighlight lang="xml" highlight="9-17">
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

In this case, the '''begin''' attribute specifies half a dozen
different values, so the animation executes several times .  Between
the '''from''' and '''to''' values, the only values that are modified
are the positions of the two control points that affect the shape of
the curve, so the animation behaves like this:

[[Image:svgGrandTour_eyeball_blink.png]]

You can use JavaScript to control these animations more flexibly. To
do so, call the '''beginElement()''' method on the animation object.
This example shifts the coordinates to which the eyes glance, with an
optional duration parameter to regulate the speed:

<syntaxhighlight lang="javascript">
function glanceTo(x,y,dur) {
    var defaultDur = 0.5;
    dur = (dur || defaultDur) + 's';
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

Enough, already?

[[Image:svgGrandTour_eyeball_tired.png]]




==Deploying SVG==

Until recently, SVG was fairly difficult to incorporate with other web
content, and there are still many challenges. The HTML5 standard
provides a way to insert ''inline'' regions of SVG into HTML files.

[[Image:scr_svg_html.png]]

It translates to this basic HTML markup structure, where CSS and
JavaScript may affect both HTML and SVG content:

<syntaxhighlight lang="xml">
<!DOCTYPE html>
<html>
  <head>
    <link href="styles/html_and_svg.css" rel="stylesheet" />
  </head>
  <body>
    <script defer type="text/javascript" src="js/html_and_svg.js">
    </script>
    <svg>
      <!-- define graphics here -->
    </svg>
  </body>
</html>
</syntaxhighlight>

There are also other ways to do it.  You can reference external SVG
files, and render them interactively within the HTML using either
'''iframe''', '''embed''', or '''object''' tags:

<syntaxhighlight lang="xml">
<!DOCTYPE html>
<html>
  <head>
    <link href="styles/html_and_svg.css" rel="stylesheet" />
  </head>
  <body>
    <script defer type="text/javascript" src="js/html_and_svg.js"></script>
    <iframe src=’graphics.svg’></iframe>
    <embed src=’graphics.svg’></embed>
    <object data=’graphics.svg’ type=’image/svg+xml’></object>
  </body>
</html>
</syntaxhighlight>

It's also common to reference external SVG files to present static SVG
graphics via CSS. The example below shows how you might place a
right-aligned navigation arrow within a mobile interface, rendering as
crisply as possible on high-resolution handsets:

[[Image:scr_svg_css.png]]

 a[href] {
     background-image    : url(img/nav_arrow.svg);
     background-position : center 0 right 10px;
     background-size     : contain;
     display             : block;
     min-height          : 2em;
     border-radius       : 0.5em;
     padding             : 0.5em;
 }

As you will see, you can also use URL anchors to reference individual
component graphics that are collected within an SVG file. This assigns
a custom bullet shape:

 ul > li {
    list-style-image     : url(img/components.svg#bullet);
 }

Less common in practice, SVG files can be viewed as standalone files,
perhaps as the target of a navigation. Any SVG file or '''svg''' tag
region can reference its own set of CSS and JavaScript, which only
applies within the SVG:

[[Image:scr_svg_svg.png]]

This example shows how to embed or reference either CSS or JavaScript
from within an SVG file:

<syntaxhighlight lang="xml">
<?xml version="1.0" standalone="no"?>
  <!-- reference CSS here: -->
<?xml-stylesheet href="css/styles.css" type="text/css"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">
<svg xmlns="http://www.w3.org/2000/svg" version="1.1" width="700px" height="500px" viewBox="0 0 1000 500">
  <defs>
    <style type="text/css">
        <![CDATA[
            /* embed CSS here */
        ]]>
    </style>
  </defs>
  <script type="application/ecmascript">
      <![CDATA[
          // embed JavaScript here
      ]]>
  </script>
  <!-- or reference JavaScript here: -->
  <script type="application/ecmascript" xlink:href="js/app.js">
  </script>
  <!-- define graphics here -->
</svg>
</syntaxhighlight>

From within an SVG, you can also reference components from other SVG
files. The example that follows shows how you might import a graphic
of a cat from another SVG file, then style it ''calico'' based on
referenced CSS:

[[Image:scr_svg_svg2svg.png]]

<syntaxhighlight lang="xml">
<?xml version="1.0" encoding="UTF-8" standalone="no"?>
<?xml-stylesheet href="css/svg_styles.css" type="text/css"?>
<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="1000" height="1000">
    <use xlink:href="components.svg#cat" class="calico"/>
</svg>
</syntaxhighlight>

You may also be able to use the '''foreignObject''' tag to render live
HTML content within an SVG graphic environment. This example uses the
'''switch''' tag to test whether the feature works, as recognized by
the tag's '''requiredExtensions''' attribute. If not, it uses fallback
'''text''':

[[Image:scr_svg_svg2html.png]]

<syntaxhighlight lang="xml">
<?xml version="1.0" standalone="yes"?>
<svg width="4in" height="3in" version="1.1" xmlns='http://www.w3.org/2000/svg'>
  <desc>use 'switch' to test if foreignObject works, otherwise render fallback 'text' content</desc>
  <switch>
    <foreignObject width="100" height="50" requiredExtensions="http://example.com/SVGExtensions/EmbeddedXHTML">
      <!-- XHTML content goes here -->
      <body xmlns="http://www.w3.org/1999/xhtml">
        <p>Here is a paragraph that requires word wrap</p>
        <iframe src="external.html">...or an iframe...</iframe>
      </body>
    </foreignObject>
    <text font-size="10" font-family="Verdana">
      <tspan x="10" y="10">Here is a paragraph that</tspan>
      <tspan x="10" y="20">requires word wrap.</tspan>
    </text>
  </switch>
</svg>
</syntaxhighlight>

<!--

 7 Coordinate Systems, Transformations and Units
    7.1 Introduction
    7.2 The initial viewport
    7.3 The initial coordinate system
    7.4 Coordinate system transformations
    7.5 Nested transformations
    7.6 The 'transform' attribute
    7.7 The 'viewBox' attribute
    7.8 The 'preserveAspectRatio' attribute
    7.9 Establishing a new viewport
    7.10 Units
    7.11 Object bounding box units
    7.12 Intrinsic sizing properties of the viewport of SVG content
    7.13 Geographic coordinate systems
    7.14 The 'svg:transform' attribute

    5.5 The 'symbol' element

 5 Document Structure
    5.6 The 'use' element
    5.8 Conditional processing
        5.8.1 Conditional processing overview
        5.8.2 The 'switch' element
        5.8.3 The 'requiredFeatures' attribute
        5.8.4 The 'requiredExtensions' attribute
        5.8.5 The 'systemLanguage' attribute
        5.8.6 Applicability of test attributes
    21.2 The 'metadata' element

    11.5 Controlling visibility

* '''display'''
* '''visibility'''

* '''color''', used to provide a potential indirect value (currentColor) for the '''fill''', '''stroke''', '''stop-color''', '''flood-color''' and '''lighting-color''' properties. (The SVG properties which support color allow a color specification which is extended from CSS2 to accommodate color definitions in arbitrary color spaces. See Color profile descriptions.)


-->

([[svg/tutorials/smarter_svg_overview|Overview]] /
[[svg/tutorials/smarter_svg_shapes|Shapes]] /
[[svg/tutorials/smarter_svg_text|Text]] /
[[svg/tutorials/smarter_svg_graphics|Graphics]] /
[[svg/tutorials/smarter_svg_filters|Filters]] /
[[svg/tutorials/smarter_svg_animation|Animation]] /
[[svg/tutorials/smarter_svg_interaction|Interaction]])

}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}