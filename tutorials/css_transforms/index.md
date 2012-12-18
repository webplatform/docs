{{Page_Title|Using CSS3 transforms}}
{{Flags
|High-level issues=Stub
|Editorial notes=[[User:Sierra]] has content intended for this page. See bug [https://www.w3.org/Bugs/Public/show_bug.cgi?id=20410 #20410]. Still to do here: 3D functions, perspective + origin, backview effects, nested transforms
}}
{{Byline}}
{{Summary_Section|CSS transforms allow you to dynamically manipulate
how content elements appear. You can move them around on the screen,
shrink or expand them, rotate them, or combine all these effects to
produce complex movements.  By themselves, transforms produce static
visual effects, but can be easily combined with CSS
[[tutorials/css_transitions|transitions]] and
[[tutorials/css_animations|keyframe animations]] to produce vibrant
interfaces. This tutorial first introduces two-dimensional transforms,
then shows you how to extend transforms into three-dimensional space.
}}
{{Tutorial
|Content===The transform property==

Transforms alter a block element's coordinates in several ways so that
they vary from where they would ordinarily appear. The
[[css/properties/transform|'''transform''']] CSS property specifies a
handful of transformation ''functions'' that can be combined any way
you wish: [[css/functions/translate()|'''translate()''']],
[[css/functions/scale()|'''scale()''']],
[[css/functions/rotate()|'''rotate()''']], and
[[css/functions/skew()|'''skew()''']].  Here is how you specify a
combination of most of the two-dimensional transforms discussed below,
along with a view of how the effect renders relative to the element's
default position:

 div.card {
    -moz-transform    : translate(50%, 10%) rotate(20deg) scale(0.75);
    -o-transform      : translate(50%, 10%) rotate(20deg) scale(0.75);
    -webkit-transform : translate(50%, 10%) rotate(20deg) scale(0.75);
    transform         : translate(50%, 10%) rotate(20deg) scale(0.75);
 }

[[Image:transform_combo.png]]

Transform properties were implemented recently enough that many
browsers only support them with ''vendor prefixes'' such as
'''-moz-''', '''-o-''', and '''-webkit-''' as shown above. Throughout
this tutorial, CSS examples only show the un-prefixed property name,
but for widest support you should apply all of them.

Functions are separated by spaces, but any additional arguments are
separated by commas.

While you can specify any number of these functions, values can't be
inherited from other style sheets. So you can't apply both of these
CSS classes to an element at the same time and expect both effects to
apply:

 div.spin   { transform: rotate(20deg); }
 div.tabled { transform: translate(100%) scale(0.5); }

Wherever you apply a transformation, any function left unspecified is
assigned a default value, so these work out the same as the less
verbose examples above:

 div.spin { transform: rotate(20deg) translate(0,0), scale(1) skew(0,0) }
 div.tabled { transform: rotate(0deg) translate(100%,0) scale(0.5) skew(0.0) }

You can also apply transforms directly to an object from JavaScript.
Here's an example in which tilting a mobile handset controls the tilt
of a screen element, using the 3D transforms described below:

 var gestural = document.querySelector('#gestural');
 window.addListener('deviceorientation', orientationHandler);
 orientationHandler = function(e) {
    gestural.style.transform = 'rotateX(' + (e.beta * -1) + 'deg) ' + 'rotateY(' + e.gamma + 'deg)';
    gestural.style.WebkitTransform = 'rotateX(' + (e.beta * -1) + 'deg) ' + 'rotateY(' + e.gamma + 'deg)';
 }

Transforms are used by several different web technologies, such as SVG
and the '''canvas''' element. Despite slight differences in how they
are implemented, they are specified in much the same way.

==2D transform functions==

The following isolates how each 2D function works. The
[[css/functions/translate()|'''translate()''']] function simply moves
an element around on the screen, much the same as when using
[[css/properties/top|'''top''']] and
[[css/properties/left|'''left''']] to position an element. This
example moves the card over to the right more than it moves it
downward:

 transform: translate(50%, 10%);

[[Image:transform_translate.png]]

The [[css/functions/translate()|'''translate()''']] function accepts
up to two ''x'' and ''y'' values to move to the right and
downward. These can specify any CSS measurement, including negative
values to move left and upward.  Percentages refer to the size of the
transformed element.  If you specify a single value, it's interpreted
as ''x'' and only moves the element horizontally.  Otherwise you can
specify separate [[css/functions/translateX()|'''translateX()''']] and
[[css/functions/translateY()|'''translateY()''']] functions. Here's
another way to express the same translation as above:

 transform: translateX(50%) translateY(10%);

The [[css/functions/scale()|'''scale()''']] function sizes an element
in decimal terms relative to a default value of 1. An element whose
scale is 2 doubles in size, while a scale of 0 vanishes into a point.
A single '''scale''' value applies to the whole element, but setting
two values lets you scale each axis independently, as you can also get
with separate [[css/functions/scaleX()|'''scaleX()''']] and
[[css/functions/scaleY()|'''scaleY()''']] functions.  The following
pairs offer different ways to produce the effects shown below:

 /* first card */
 transform: scale(0.75);
 transform: scale(0.75, 0.75);
 /* second card */
 transform: scale(0.75, 1.25);
 transform: scaleX(0.75) scaleY(1.25);

[[Image:transform_scale.png]]

The [[css/functions/rotate()|'''rotate()''']] function spins an
element around its ''z'' axis.  It accepts a degree ('''deg''') or
radian ('''rad''') measurement. (Radians are equivalent to the number
of degrees multiplied by &pi;/180.) Radial measurements can wrap
around, so the following values are equivalent:

 transform: rotate(20deg);
 transform: rotate(380deg);  /*   360  + 20 */
 transform: rotate(-340deg); /* (-360) + 20 */

[[Image:transform_rotate.png]]

The [[css/functions/skew()|'''skew()''']] function leans an element
over, altering its corner angle relative to the default 90&deg; and
transforming the underlying rectangle into a parallelogram.  It
accepts up to two degree ('''deg''') or radian ('''rad''')
measurements.  The separate [[css/functions/skewX()|'''skewX()''']]
function tips the side edges of the element, while
[[css/functions/skewY()|'''skewY()''']] tips the top and bottom.
Setting a single [[css/functions/skew()|'''skew()''']] value affects
only the ''x'' axis.

 transform: skewX(10deg);               /* 1st */
 transform: skewY(-30deg);              /* 2nd */
 transform: skew(10deg, -30deg);        /* 3rd */
 transform: skewX(10deg) skewY(-30deg); /* 3rd, alternate syntax */

[[Image:transform_skew.png]]

Note that combining ''x'' and ''y'' skews makes the element appear to
move into three-dimensional space, but the transformation actually
occurs within a flat plane. Skip below for information about 3D
transforms.

'''Note:''' Browsers internally represent all of the transformations
described above as a single ''matrix'' expression, which for 2D
transforms consist of six values.  Using the web inspector feature,
you can view any transformed element's computed style for an example,
and use the the alternative [[css/functions/matrix()|'''matrix()''']]
function to specify those values.  Here is how the ace of spades in
the example above is represented as a matrix value:

 transform: matrix(1, -0.577, 0.176, 1, 0, 0);

==You need some perspective==

You really do.  Though they often take on the illusion of three
dimensions, 2D transforms are strictly superficial, inhabiting the
plane of the display screen. Three dimensional transforms allow
ordinary web content, which is still inherently flat, to shift onto
other planes.  But before applying the 3D transform functions
discussed below, you need to position the scene relative to the
viewer.

Applying ''perspective'' to an an element indicates the viewer's
perceived distance to any transformed descendent elements.  The
[[css/properties/perspective|'''perspective''']] property sets a
number of CSS pixels along the ''z'' axis that leads from the screen
to the viewer.  Since ordinary web content is inherently flat, all
measurements along the ''z'' axis ''must'' specify absolute units such
as pixels, rather than relative percentages that make sense along
''x'' and ''y''.

The default [[css/properties/perspective|'''perspective''']] value of
'''none''' indicates an infinite perspective, which appears flat.  A
value in the range of 1000 to 2000 mimics the distance at which people
typically view their screen.  Perspective values of less than 1000
appear increasingly distorted, but may be desirable for immersive
virtual reality applications in which the viewer appears to mingle
among displaying elements.

The first scene in the example below shows a 3D rotation that appears
flat before applying [[css/properties/perspective|'''perspective''']],
while the second shows a distance of 1000.  The ancestor element's
[[css/properties/border|'''border''']] reveals how the descendant's
plane has shifted.

<pre>
.parent {
    border		: thin solid #000;
    perspective		: 1000;
    perspective-origin	: 50% 50%;
}
.child {
    transform		: rotateY(45deg);
}
</pre>

[[Image:transform_perspective.png]]

While [[css/properties/perspective|'''perspective''']] affects the
perceived distance to an object along the ''z'' axis, the
[[css/properties/perspective-origin|'''perspective-origin''']]
property allows you to shift the perceived location along ''x'' and
''y'' from which it is viewed. The second scene reflects the default
'''center''' value in which the viewpoint is centered straight out
from the screen.  Altering these values positions the viewer
diagonally from the scene.  The third scene shows the same rotation,
but with the viewpoint shifted to the right:

 perspective-origin-x : 500px;

This only affects how the transformed element appears, not the
ancestor that specifies the perspective.  Note that since percentages
refer to the size of the transformed element, pixel units may be
easier to use.
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
|Topic_clusters=Transforms
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}