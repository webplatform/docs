{{Page_Title|SVG: Grand Tour}}
{{Flags
|High-level issues=Stub
|Editorial notes=[new content edited offline by Sierra ([[User:Sierra|Sierra]] ([[User talk:Sierra|talk]])); please do not edit]
}}
{{Byline
|Name=Mike Sierra 
}}
{{Summary_Section|This guide introduces SVG graphics and shows you all the basics of how to deploy them along with standard web content.}}
{{Tutorial
|Content=SVG is a standard XML markup format that renders ''Scalable
Vector Graphics'' within web browsers.  Vector or ''drawing''-style
graphics are implemented as pure shapes that render crisply at any
magnification. In contrast, ''raster'' or ''paint''-style images
consist of a series of pixels that may not display well when zoomed at
high resolution.  Use SVG if you want to freely interact with portions
of a graphic.  Since SVG renders within the browser's DOM, each
graphic component can be styled through CSS, manipulated with
JavaScript through core APIs, and can appear comfortably alongside
HTML content.

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
'''cx''', '''cy''', and '''r''' attributes position and size it:

<syntaxhighlight lang="xml">
<circle id="eyeball" cx="100" cy="100" r="150"/>
</syntaxhighlight>

[[Image:svg_overview_eyeball_nofill.png]]

By default, it's filled black. While you can apply a solid color, a
more complex radial gradient happens to be the ideal way to build the
eyeball's series of concentric rings:

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

[[Image:svg_overview_eyeball_fill.png]]

The '''circle''' tag's '''fill''' attribute references the '''id''' of
the '''radialGradient'''.  The various nested '''stop''' tags define
fairly abrupt gradations from the center to the edge&mdash;from black
to blue and then to white&mdash;followed by a more gradual transition
to pink around the edge of the circle.

In this example, the '''id''' and '''offset''' are ordinary
''attributes'', while the '''stop-color''' is known as a
''presentation attribute''.  These are simply CSS properties that are
expressed as attributes.  Other than the tendency of CSS property
names to use dashes-between-lowercase-words rather than ''camelCase''
for attribute names, there may be no way to tell the difference by
looking at them.

Many CSS properties such as '''stop-color''' apply only to SVG
content. Some, like '''font-size''', apply to both SVG and HTML.  Some
behave like CSS properties that you apply to HTML, but are named
differently. The '''fill''' property provides much the same
capabilities in SVG as the '''background-color''' and
'''background-image''' properties does in HTML.  Since
'''stop-color''' is CSS, You can also modify it locally via the
'''style''' attribute. Doing so actually takes precedence over the
value of presentation attributes, so this example changes the eye
color to brown:

<syntaxhighlight lang="xml">
<stop id="pupil" offset="15%" stop-color="lightblue" style="stop-color:brown"/>
</syntaxhighlight>

It's best practice to consolidate CSS in style sheets and separate it
from markup. Placing this CSS in the ''eyeballs.css'' file referenced
from the HTML applies it to the slightly pared-down SVG markup that
follows:

<syntaxhighlight lang="css">
 #inner { stop-color                   : black; }
 #outer { stop-color                   : pink; }
 #white, #bloodshotExtent { stop-color : white; }
 .blue { stop-color                    : lightblue; }
 .brown { stop-color                   : brown; }
</syntaxhighlight>

<syntaxhighlight lang="xml">
<radialGradient id="eyeballFill">
  <stop id="inner"           offset="12%"  />
  <stop id="pupil"           offset="15%"  class="blue" />
  <stop id="iris"            offset="27%"  class="blue" />
  <stop id="white"           offset="30%"  />
  <stop id="bloodshotExtent" offset="40%"  />
  <stop id="outer"           offset="100%" />
</radialGradient>
</syntaxhighlight>

==Referencing graphics==

The circle is much larger than the actual eyeball, because we want it
to float behind a pair of eyelids. Before you build them, however, you
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
'''circle''' still references it as before.  If you move the
'''circle''' there, it doesn't render. To get it to appear again later
after you've built other components, you don't have to move it back
out. Instead, place this line outside the '''defs''' region:

<syntaxhighlight lang="xml">
<use xlink:href="#eyeball"/>
</syntaxhighlight>

This serves as a pointer to the eyeball graphic.  It's a ''deep''
reference, not just a copy. That means any changes made to the
'''circle''' or '''radialGradient''' within the '''defs''' appears
dynamically. Still, the '''use''' tag allows you to add attributes or
override those defined in the prototype component. This example
specifies a new '''id''' and modifies the '''cx''' attribute to move
it to the left a bit from its original position at ''100'':

<syntaxhighlight lang="xml">
<use  xlink:href="#eyeball" id="eyeballLeft" cx="80"/>
</syntaxhighlight>

The '''transform''' attribute's '''translate()''' function provides a
more flexible way to reposition objects referenced via '''use'''. It
uses relative measurements to move it to the left along the ''x''
axis, and not at all along the ''y'' axis:

<syntaxhighlight lang="xml">
<use xlink:href="#eyeball" id="eyeballLeft" transform="translate(-20,0)"/>
</syntaxhighlight>

These provide the same functionality as two-dimensional CSS
transforms.  The '''scale()''' function accepts a decimal value to
size the object, where ''1'' is the current size, ''0'' vanishes to a
point, and values greater than 1 increase the size.  The
'''rotate()''' function accepts a ''deg'' or ''rad'' measurement that
spins the object.  The '''skewX()''' and '''skewY()''' also accepts an
angle with which to shear the object horizontally or vertically.

==The eyelids==

To place the eyeball within eyelids requires a ''clipping path'',
which allows an object to render only when it appears within another
shape. In this case, the ''eyelids'' shape is a free-form '''path'''
whose '''d''' (''definition'') draws two curves that face each other:

<syntaxhighlight lang="xml">
<path
    id           = "eyelids"
    d            = "M 200,100 Q 100,200 0,100 Q 100,0 200,100"
    fill         = "transparent"
    stroke       = "black"
    stroke-width = "2"
/>
</syntaxhighlight>

[[Image:svg_overview_eyeball_eyelid.png]]

Part of each curve's definition is a ''control point'' that influences
that shape of the curve, but do not themselves render. Starting from
the right corner (''M'' for ''move to''), the first quadratic (''Q'')
curve's control point is placed at the top, and the destination is the
left corner. The second quadratic curve places its control point at
the bottom corner and ends up at the right corner:

[[Image:svg_overview_eyeball_ctrl.png]]

To make the shape behave as a clipping path, place a '''clipPath'''
tag around the '''path'''. You will actually need to use this shape
again, so it is best to '''use''' a reference to it:

<syntaxhighlight lang="xml">
<clipPath id="clipEyelid">
    <use xlink:href="#eyelids" />
</clipPath>
</syntaxhighlight>

Now apply the '''clip-path''' attribute to the eyeball shape for the
clipping path to take effect. You can apply it to the original shape,
or the '''use''' that references it:

<syntaxhighlight lang="xml">
<use xlink:href="#eyeball" clip-path="url(#clipEyelid)" />
</syntaxhighlight>

[[Image:svg_overview_eyeball_eyelid_clip.png]]

The only problem now is that the eyelid disappeared. Clipping paths
don't actually render, so the solution is to draw another reference to
it.  The first '''use''' below renders the eyeball within the clipping
path, and the second renders the path:

<syntaxhighlight lang="xml">
<g id="eye">
  <use xlink:href="#eyeball" clip-path="url(#clipEyelid)" />
  <use xlink:href="#eyelids" />
</g>
</syntaxhighlight>

[[Image:svg_overview_eyeball_eyelid_both.png]]

It becomes useful here to wrap a '''g''' tag to ''group'' the two
graphic elements into a larger semantic ''eye'' object. You can then
move or otherwise transform them as a unit.

==The eyelashes==

To draw eyelashes, there are potentially a couple of ways to attach
objects to the ''eyelid'' path. One is to define a ''marker'', which
wouldn't work here because the graphic would only appear at each
corner of the eye. Another is to run text along the path, which may
seem odd but in this case provides the illusion we want.  First, place
many lowercase ''l'' characters within a '''text''' element, enough to
overflow the ''eyelids'' shape:

<syntaxhighlight lang="xml">
<text id="eyelashContent" >
llllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllll
</text>
</syntaxhighlight>

The '''tref''' tag inserts the referenced ''eyelashContent'' text
within a '''textPath''' wrapper that itself references the ''eyelids''
shape along which to run the text.  The outer ''eyelashes'' wrapper is
necessary to render the entire collection of text, some of which may
run along a path. Various '''tref''' attributes slant the text,
lighten it, and space it out:

<syntaxhighlight lang="xml" highlight="2,5">
<text id="eyelashes">
  <textPath xlink:href="#eyelids">
    <tref
      id               = "eyelashTextRef"
      xlink:href       = "#eyelashContent"
      font-size        = "20"
      letter-spacing   = "4"
      font-style       = "italic"
      stroke           = "#ddd"
    />
  </textPath>
</text>
</syntaxhighlight>

Add the eyelashes to the consolidated ''eye'' object:

<syntaxhighlight lang="xml">
<g id="eye">
  <use xlink:href="#eyeball" clip-path="url(#clipEyelid)" />
  <use xlink:href="#eyelids" />
  <use xlink:href="#eyelashes" />
</g>
</syntaxhighlight>

[[Image:svg_overview_eyeball_eyelashes.png]]

==Applying eyeliner==

Even after lightening the color, the eyelashes appear way too crisp
and detailed compared to the eyeball, and could be softened up a bit.
SVG ''filters'' provide many image processing tools that you can mix
and match to produce such special visual effects.

Add a '''filter''' element to the '''defs''' region. It serves as a
wrapper for various ''filter effect'' components, which are applied in
sequence. In this case, the '''feGaussianBlur''' effect scatters the
pixels around, and '''feComponentTransfer''' darkens the result:

<syntaxhighlight lang="xml">
<filter
    id           = "soften"
    x            = "-20"
    y            = "-20"
    width        = "250"
    height       = "250"
    filterUnits  = "userSpaceOnUse"
>
  <desc>soften eyelidand eyelashes</desc>
  <feGaussianBlur stdDeviation="1 3" />
  <feComponentTransfer>
      <feFuncR type="linear" slope="0.3"/>
      <feFuncG type="linear" slope="0.3"/>
      <feFuncB type="linear" slope="0.3"/>
  </feComponentTransfer>
</filter>
</syntaxhighlight>

The eyelid renders horizontally between 0 and 200 pixels, so the
eyelashes spill slightly outside the the left edge of the original
drawing area.  The ''filter'' tag's
'''x'''/'''y'''/'''width'''/'''height''' attributes apply the effect
to a wider set of dimensions. Setting '''filterUnits''' to
'''userSpaceOnUse''' specifies to use the original coordinate system;
otherwise values would be interpreted as percentages of the box to
which the filter is applied.

Use the '''filter''' attribute to apply the effect, in this case to
the eyelashes:

<syntaxhighlight lang="xml" highlight="3">
<text
    id     = "eyelashes"
    filter = "url(#soften)"
/>
</syntaxhighlight>

[[Image:svg_overview_eyeball_eyelash_filter.png]]

It needs to be applied again separately to the eyelids:

<syntaxhighlight lang="xml" highlight="4">
<path
    id           = "eyelids"
    d            = "M 200,100 Q 100,200 0,100 Q 100,0 200,100"
    filter       = "url(#soften)"
    fill         = "transparent"
    stroke       = "#aaa"
    stroke-width = "2"
/>
</syntaxhighlight>

[[Image:svg_overview_eyeball_eyelid_filter.png]]

==Coordinate spaces==

To finish off the graphic, group another instance of the ''eye''
object into a higher-level ''eyes'' object, and use '''transform''' to
space them out:

<syntaxhighlight lang="xml">
<g id="eyes">
  <use xlink:href="#eye" transform="translate(50,0)" />
  <use xlink:href="#eye" transform="translate(350,0)" />
</g>
</syntaxhighlight>

A single '''use''' tag outside the '''defs''' region renders the eyes:

<syntaxhighlight lang="xml">
<use xlink:href="#eyes"/>
</syntaxhighlight>

[[Image:svg_overview_eyeballs.png]]

The original '''svg''' tag specified that the eyes should appear
within a 600&times;200-pixel rectangle:

<syntaxhighlight lang="xml">
<svg width="600" height="200">
</syntaxhighlight>

[[Image:svg_overview_eyeballs_viewport_large.png]]

But what if that's much too big for the interface where you want to
use them? If you shrink it down, using either the tag's
'''width'''/'''height''' attributes or CSS, the dimensions no longer
match the various measurements specified within the graphic:

<syntaxhighlight lang="xml">
<style>
svg {
    width: 300;
    height: 100;
}
</style>
    <!-- ...or... -->
<svg width="300" height="100">
</syntaxhighlight>

[[Image:svg_overview_eyeballs_viewport_small.png]]

The solution is to define a custom box using the '''viewBox'''
attribute.  Doing so declares a set of abstract units for use within
the graphic, which may bear no relation to the coordinate space in
which the graphic appears:

<syntaxhighlight lang="xml">
<svg width="300" height="100" viewBox="0 0 600 200">
</syntaxhighlight>

[[Image:svg_overview_eyeballs_viewbox.png]]

Adding a '''preserveAspectRatio''' attribute controls what happens in
cases when the '''viewBox''' doesn't match the ''viewport'' within
which the graphic appears. In this case, '''xMidYMid''' centers it and
shrinks it enough for the entire graphic to appear:

<syntaxhighlight lang="xml">
<svg width="100" height="100" viewBox="0 0 600 200" preserveAspectRatio="xMidYMid">
</syntaxhighlight>

[[Image:svg_overview_eyeballs_viewbox_preserve.png]]

==Blinking and glancing==

The only remaining problem is that the graphic doesn't ''do''
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

You can't use that familiar approach for SVG attributes.  SVG has its
own mechanism (based on the ''SMIL'' standard) to animate attribute
values. We'll use it to make the eye glance to the side. As we've
seen, the '''transform''' attribute's '''translate()''' function
offers the most flexible way to move objects around. SVG provides an
'''animateTransform''' tag dedicated to manipulating it. Add it within
the ''eyeball'' object you want to move:

<syntaxhighlight lang="xml" highlight="3-12">
<circle id="eyeball" transform="translate(0,0)" cx="100" cy="100"
        r="150" fill="url(#eyeballFill)">
    <animateTransform
        id             = "glanceStart"
        attributeType  = "XML"
        attributeName  = "transform"
        type           = "translate"
        begin          = "1s"
        dur            = "0.5s"
        from           = "0 0"
        to             = "50 0"
    />
</circle>
</syntaxhighlight>

Let's run down what each attribute does:

* '''attributeType''' clarifies that the value we're manipulating is an ''XML'' attribute, not a ''CSS'' property.

* '''attributeName''' provides the name of the attribute to modify, ''transform'' in this case.

* Since a transform can specify combinations of functions, the '''type''' attribute clarifies which function to manipulate, ''translate'' in this case.

* '''begin''' specifies a delay after which the animation executes, in this case 1 second. A begin value of ''0s'' animates immediately. (If you leave out this attribute, the animation does not play by default, but you can use JavaScript to make it play as described below.)

* '''dur''' specifies the animation's duration, half a second in this case.

* '''from''' and '''to''' provide the values between which the animation should transition. In this case, it moves it 50 units to the right.

As it appears above, the animation moves the eyes to the right, then
immediately snaps back:

[[Image:svg_overview_eyeball_glance.png]]

There's an attribute called '''fill''', which is unfortunately named
the same as the '''fill''' property that applies colors and
gradients. Adding a '''fill''' attribute here and setting it to
'''freeze''' would keep the eyes looking right after the animation
ends.  But instead, we'll add another animation to return the eyes so
that they look ahead:

<syntaxhighlight lang="xml" highlight="4,19-20">
<circle id="eyeball" transform="translate(0,0)" cx="100" cy="100"
        r="150" fill="url(#eyeballFill)">
    <animateTransform
        id             = "glanceStart"
        attributeType  = "XML"
        attributeName  = "transform"
        type           = "translate"
        begin          = "1s"
        dur            = "0.5s"
        from           = "0 0"
        to             = "50 0"
    />
    <animateTransform
        id             = "glanceEnd"
        attributeType  = "XML"
        attributeName  = "transform"
        type           = "translate"
        dur            = "0.5s"
        begin          = "glanceStart.end"
        from           = "50 0"
        to             = "0 0"
    />
</circle>
</syntaxhighlight>

Aside from the values of '''from''' and '''to''' being inverted, note
the '''begin''' time is expressed in terms of whenever the previous
animation ends.  And yes, it may help to keep track of the three
different ways we've seen so far to reference an SVG object:

* the ''id.attr'' notation above.

* SVG's '''xlink:href''', which specifies a URL, external file, or anchor.

* CSS's own '''url()''' function, which can be applied to SVG's presentation attribute values.

As is true for CSS transitions and animations, you can animate most
any numeric or color value. You can also animate complex series of
coordinates used in '''path''' definitions, so long as the sequence of
path commands match so that there are corresponding sets of points.
This allows us to make the eyes blink. Add this to the ''eyelids''
object:

<syntaxhighlight lang="xml" highlight="9-17">
<path
    filter       = "url(#soften)"
    id           = "eyelids"
    d            = "M 200,100 Q 100,200 0,100 Q 100,0 200,100"
    fill         = "transparent"
    stroke       = "#aaa"
    stroke-width = "2"
>
    <animate
        id            = "blink"
        attributeType = "XML"
        attributeName = "d"
        from          = "M 200,100 Q 100,200 0,100 Q 100,0 200,100"
        to            = "M 200,100 Q 100,100 0,100 Q 100,100 200,100"
        begin         = "4s;6s"
        dur           = "0.1s"
    />
</path>
</syntaxhighlight>

In this case, the '''begin''' attribute specifies two different
values, so the animation is triggered after four seconds, then once
again after six seconds.  Between the '''from''' and '''to''' values,
the only values that are modified are the positions of the two control
points that affect the shape of the curve, so the animation behaves
like this:

[[Image:svg_overview_eyeball_blink.png]]

You can use JavaScript to control these animations more flexibly. To
do so, call the '''beginElement()''' method on the animation object.
This allows a script to change where the eyes glance:

<syntaxhighlight lang="javascript">
function glanceTo(x,y) {
    var toThere = document.querySelector('#glanceStart')
    var andBack = document.querySelector('#glanceEnd')
    toThere.setAttribute("to", x + " " + y);
    andBack.setAttribute("from", x + " " + y);
    toThere.beginElement();
}
</syntaxhighlight>

Calling this function keeps the eyes blinking at random points between
two and five seconds:

<syntaxhighlight lang="javascript">
function blink() {
    var minDelay = 2000;
    var extraDelay = 3000;
    document.querySelector('#blink').beginElement();
    setTimeout(blink, (Math.floor(Math.random() * extraDelay) + minDelay));
}
</syntaxhighlight>

Enough, already?

[[Image:svg_overview_eyeball_tired.png]]

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