{{Page_Title|SVG animation}}
{{Flags
|High-level issues=Stub
|Checked_Out=Yes
}}
{{Byline
|Name=Mike Sierra
}}
{{Summary_Section|This guide shows you how to animate SVG graphics using SMIL-based markup. Along with standard animation techniques, you will learn how to morph shapes, move graphics along a curve, animate complex filter effects, and control animations from JavaScript.}}
{{Tutorial
|Content=Interfaces become more vibrant once you add animation
effects.  This guide focuses on SVG's built-in animation features,
which derive from SMIL, the ''Synchronized Multimedia Integration
Language''.  As discussed in the
[[svg/tutorials/smarter_svg_overview|SVG grand tour]], many SVG
attributes are actually implemented as CSS ''properties'', and thus
respond to CSS [[tutorials/css_transitions|transitions]] and
[[tutorials/css_animations|keyframe animations]]. The techniques
described here offer a way to animate SVG ''attributes'', but can be
used for ''properties'' as well. You'll also learn how to dynamically
modify any attribute values that can't be animated.

==A simple animation==

Start with a simple element that you'd like to animate:

<syntaxhighlight lang="xml">
<text x="0" y="100">An SVG Animation</text>
</syntaxhighlight>

Nest an [[svg/elements/animate|'''animate''']] element such as the
following:

<syntaxhighlight lang="xml" highlight="3-9">
<text x="0" y="100">
    An SVG Animation
    <animate
        attributeName = "x"
        from          = "1000"
        to            = "0"
        begin         = "0s"
        dur           = "0.5s"
        id            = "swipe"
    />
</text>
</syntaxhighlight>

When you load the SVG, the resulting animation quickly swipes in some
text from the right side of the screen:

[[Image:svga_simpleSwipe.png|400px]]

Each animation element can only modify the value of one attribute at a
time, specified by the
[[svg/attributes/attributeName|'''attributeName''']]. The
[[svg/attributes/from|'''from''']] and [[svg/attributes/to|'''to''']]
set what the values of that attribute should be at the beginning and
end of the animation.
Setting the [[svg/attributes/begin|'''begin''']] to '''0s''' makes it
execute immediately, and the [[svg/attributes/dur|'''dur''']] sets a
half-second duration over which the animation executes.

Instead of nesting the animation, you can also indirectly link the
element you want to animate. However, the animation can ''only'' be
applied to a single element, so this represents only a superficial
difference:

<syntaxhighlight lang="xml">
<defs>
<animate id="swipe" xlink:href="#swipeText" attributeName="x"
         from="1000" to="0" begin="0s" dur="0.5s" />
</defs>
<text id="swipeText" x="0" y="100">An SVG Animation</text>
</syntaxhighlight>

[http://letmespellitoutforyou.com/samples/svg/anim_swipe.svg View this animation]

==Delaying an animation==

Increasing the [[svg/attributes/begin|'''begin''']] attribute's time
value from '''0s''' to '''1s''' delays the animation:

<syntaxhighlight lang="xml" highlight="1,7,9">
<text x="1000" y="100">
    An SVG Animation
    <animate
        attributeName = "x"
        from          = "1000"
        to            = "0"
        begin         = "1s"
        dur           = "0.5s"
        fill          = "freeze"
        id            = "delayed_swipe"
    />
</text>
</syntaxhighlight>

But notice there's a problem, and the fix is highlighted.  The outer
text element's '''x''' attribute is now set to '''1000'''. If you kept
it at '''0''', the text would display for a second, then awkwardly
disappear once the animation starts to execute, slide in from the
right, and reposition itself at its initial location.

Fixing that problem causes another problem, whose solution is also
highlighted. Once the animation completes, the value of '''x'''
reverts to its initial value, '''1000''', thus making it disappear.
Setting the [[svg/attributes/fill|'''fill''']] attribute to
'''freeze''' maintains the attribute's value after the animation
completes, effectively overriding whatever the text element specifies.
(The [[svg/attributes/fill|'''fill''']] ''attribute'' is unfortunately
named the same as SVG's [[svg/properties/fill|'''fill''']]
''property'', which specifies background colors and images. Do not
get the two mixed up.)

[http://letmespellitoutforyou.com/samples/svg/anim_swipeDelay.svg View this animation]

==Sequences of frames==

This animation swipes in, but then comes to an abrupt stop.  This more
natural-looking variation bounces the text a bit off the left wall:

<syntaxhighlight lang="xml" highlight="9-10">
<animate
    id            = "bounce"
    attributeName = "x"
    from          = "1000"
    to            = "0"
    begin         = "0s"
    dur           = "0.5s"
    fill          = "freeze"
    values        = "1000;0;-20;10;0"
    keyTimes      = "0;0.8;0.85;0.9;1"
/>
</syntaxhighlight>

The highlighted [[svg/attributes/values|'''values''']] attribute uses
semicolons to specify a series of intermediate values between the
animation's [[svg/attributes/begin|'''begin''']] and
[[svg/attributes/end|'''end''']] points. Starting at '''1000''', the
animation proceeds to the '''0''' point that represents the left wall,
then goes a bit further to '''-20''', then back to '''10''' before
finally settling at '''0'''.

The [[svg/attributes/values|'''values''']] specification by itself
would still an awkward result. The initial transition between
'''1000''' and '''0''' executes ''very'' quickly, after which the
subsequent transitions seem much too slow. The
[[svg/attributes/keyTimes|'''keyTimes''']], fixes this by
[[svg/attributes/keyTimes|'''keyTimes''']] specifying the share of
time, between 0 and 1, each segment should take to execute. In this
case, the initial transition that slides the text in takes 80% of the
total duration, rather than the more brisk 25% default range between
the five values.  The number of
[[svg/attributes/keyTimes|'''keyTimes''']] must match the number of
[[svg/attributes/values|'''values''']], or the animation does not
work.

[http://letmespellitoutforyou.com/samples/svg/anim_swipeFrames.svg View this animation]

==Synchronizing animations==

The example above simply manipulates a single attribute that positions
an element.  Animations become far more interesting when applied to
complex filter effects. This variation synchronizes two different
animations, swiping horizontally blurred text into view, then removing
the blur once it has stopped:

[[Image:svga_xBlur.png|400px]]

It is based on the following filter:

<syntaxhighlight lang="xml" highlight="2,3">
<filter id="slidingBlur">
  <feOffset       id="slideEffect" dx="1000" dy="0" />
  <feGaussianBlur id="blurEffect" stdDeviation="20,1" />
</filter>
</syntaxhighlight>

The [[svg/elements/feOffset|'''feOffset''']] effect's
[[svg/attributes/dx|'''dx''']] value reproduces the slide effect using
the techniques discussed above, moving the element horizontally within
the filtered region:

<syntaxhighlight lang="xml" highlight="2,3">
<animate
    id            = "slideAnim"
    attributeName = "dx"
    from          = "1000"
    to            = "0"
    begin         = "0s"
    dur           = "0.5s"
    fill          = "freeze"
    values        = "1000;0;-20;10;0"
    keyTimes      = "0;0.8;0.85;0.9;1"
    xlink:href    = "#slideEffect"
/>
</syntaxhighlight>

The [[svg/elements/feGaussianBlur|'''feGaussianBlur''']] effect uses
its [[svg/attributes/stdDeviation|'''stdDeviation''']] to control the
degree of blur, and the animation reduces it primarily along the ''x''
axis. But note its [[svg/attributes/begin|'''begin''']] attribute no
longer specifies a time value. Instead, this animation begins whenever
the previous one ends:

<syntaxhighlight lang="xml" highlight="6">
<animate
    id            = "blurAnim"
    attributeName = "stdDeviation"
    from          = "20,1"
    to            = "0,0"
    begin         = "slideAnim.end"
    dur           = "0.2s"
    fill          = "freeze"
    xlink:href    = "#blurEffect"
/>
</syntaxhighlight>

The ''slideAnim'' identifies the previous animation, and the ''.end''
refers to the [[dom/events/end|'''end''']] DOM event the animation
produces. Referencing the corresponding
[[dom/events/begin|'''begin''']] event likewise allows you to execute
different animations concurrently, without having to keep overall
track of how long each one takes to keep them all synchronized.

To calculate when to start the second animation, SVG actually looks
ahead to see when the [[dom/events/end|'''end''']] event is supposed
to occur. You can subtract or add time values to start it before or
after that point. For example, this variation overlaps the two
animations by a fifth of a second:

 begin = "slideAnim.end-200ms"

To maintain long chains of animations, you can also use the '''prev'''
keyword, which refers to the previously defined animation:

 begin = "prev.end"

[http://letmespellitoutforyou.com/samples/svg/anim_swipeBlur.svg View this animation]

==Morphing shapes==

The motion animation shown above animates a single value at a time,
but the blur animation animates two, a pair of coordinates. SVG also
allows you to animate long series of coordinates that make up
[[svg/elements/path|'''path''']] definitions, resulting in curved
morphing effects:

<div style="display:inline-block">
[[Image:svga_morph1.png|200px]]
</div>
<div style="display:inline-block">
[[Image:svga_morph2.png|200px]]
</div>
<div style="display:inline-block">
[[Image:svga_morph3.png|200px]]
</div>
<div style="display:inline-block">
[[Image:svga_morph4.png|200px]]
</div>

For the animation to work, the [[svg/attributes/from|'''from''']] and
[[svg/attributes/to|'''to''']] values, as well as any frames specified
along the way in [[svg/attributes/values|'''values''']], must feature
the exact same number of path commands, all arranged in the same
sequence. Only their numeric values may vary.  This example shows a
path consisting of one ''M'' positioning command and four ''S'' curve
commands going through a series of eight frames:

<syntaxhighlight lang="xml">
<path id = "shape" d = "M 115,169 S 149,424 460,555 S 608,367 568,157
      S 438,108 174,57 S 97,90 115,169" >
<animate attributeName = "d" begin = "0s" dur = "20s"
  from = "M 115,169 S 149,424 460,555 S 608,367 568,157 S 438,108 174,57 S 97,90 115,169"
  to = "M 115,169 S 149,424 460,555 S 608,367 568,157 S 438,108 174,57 S 97,90 115,169"
  values = "M 115,169 S 149,424 460,555 S 608,367 568,157 S 438,108 174,57 S 97,90 115,169;M
    284,81 S 117,248 91 ,478 S 240,595 547,608 S 608,349 588,140 S 420,48 284,81;M
    360,313 S 413,253 475,308 S 491,422 464,508 S 293,511 217,424 S 254,297 360,313;M
    381,643 S 574,490 580,225 S 468,133 297,38 S 103,144 62,382 S 172,641 381,643;M
    456,56 S 579,221 603,479 S 449,59 5 196,636 S 64,367 96,111 S 371,28 456,56;M
    552,89 S 326,83 111,219 S 66,407 104,623 S 426,653 605,503 S 655,263 552,89;M
    628,3 55 S 563,183 397,79 S 199,79 65,270 S 65,464 258,650 S 467,623 628,355;M
    84,239 S 223,528 336,620 S 516,606 630,347 S 587,153 3 25,70 S 76,87 84,239;M
    115,169 S 149,424 460,555 S 608,367 568,157 S 438,108 174,57 S 97,90 115,169"
/>
</path>
</syntaxhighlight>

[http://letmespellitoutforyou.com/samples/svg/anim_morph.svg View this animation]

==Setting the pace==

This variation on the swipe animation doesn't bounce it against the
wall, but instead brings the text to a more gradual stop:

<syntaxhighlight lang="xml" highlight="9-10">
<animate
    id            = "ease_in"
    attributeName = "x"
    from          = "1000"
    to            = "0"
    begin         = "1s"
    dur           = "0.5s"
    fill          = "freeze"
    calcMode      = "spline"
    keySplines    = "0 0.75 0.25 1"
    keyTimes      = "0;1"
/>
</syntaxhighlight>

By default, animations progress as a constant rate.  Setting the
[[svg/attributes/calcMode|'''calcMode''']] to '''spline''' makes it
respond to a bezier curve, defined by the value of
[[svg/attributes/keySplines|'''keySplines''']]. You can use semicolons
to specify as many curves as there are frames in your animation.

The following examples show how these response curves behave, usually
by slowing the start and end points.  Each ''x'' axis represents the
animation's elapsed time, and the ''y'' axis represents its progress,
so the more the line curves vertically along the way, the faster the
animation proceeds at that point.

<div style="display:inline-block;max-width:170px">
 0.42 0 1 1
 ease-in
[[Image:transitF_easein.png]]
</div>

<div style="display:inline-block;max-width:170px">
 0 0 0.58 1
 ease-out
[[Image:transitF_easeout.png]]
</div>

<div style="display:inline-block;max-width:170px">
 0.25 0.1 0.25 1
 ease
[[Image:transitF_ease.png]]
</div>

<div style="display:inline-block;max-width:170px">
 0.42 0 0.58 1
 ease-in-out
[[Image:transitF_easeinout.png]]
</div>

<div style="display:inline-block;max-width:170px">
 0 0 1 1
 linear
[[Image:transitF_linear.png]]
</div>

These examples compare common
[[css/properties/transition-timing-function|'''transition-timing-function''']]
and
[[css/properties/animation-timing-function|'''animation-timing-function''']]
CSS property keywords with their
[[css/functions/cubic-bezier|'''cubic-bezier()''']] CSS function
equivalents.

If [[svg/attributes/calcMode|'''calcMode''']] is set to
'''discrete''', the animation jumps abruptly from each frame defined
in [[svg/attributes/values|'''values''']] to the next, just like CSS's
[[css/functions/steps|'''steps()''']] function. If it's set to
'''paced''', it progresses at a constant rate over the entire course
of the animation, but unlike '''linear''', it ignores any progress
points [[svg/attributes/keyTimes|'''keyTimes''']] may define along the
way.

[http://letmespellitoutforyou.com/samples/svg/anim_swipeTimed.svg View this animation]

==Repetition==

The examples above all execute once, but this example uses
[[svg/attributes/repeatCount|'''repeatCount''']] to run an animation
continuously.  It modifies a more complex filter effect (explained in
greater detail in [[svg/tutorials/smarter_svg_filters|SVG Filters]])
that shines a light on a beveled surface:

<syntaxhighlight lang="xml" highlight="4,6">
<filter id="bevel" filterUnits="userSpaceOnUse">
  <feGaussianBlur in="SourceAlpha" stdDeviation="4" result="blur"/>
  <feOffset in="blur" dx="4" dy="4" result="offsetBlur"/>
  <feSpecularLighting id="elevationEffect" surfaceScale="20" specularConstant=".75"
        in="blur" result="specOut" specularExponent="20" lighting-color="#bbbbbb" >
    <feDistantLight id="lightAngleEffect" azimuth="0" elevation="30" />
  </feSpecularLighting>
  <feComposite in="specOut" in2="SourceAlpha" operator="in" result="specOut"/>
  <feComposite in="SourceGraphic" in2="specOut" operator="arithmetic" result="litPaint"
        k1="0" k2="1" k3="1" k4="0" />
  <feComposite in="litPaint" in2="offsetBlur" operator="over"/>
</filter>
</syntaxhighlight>

[[Image:svga_bevel.png]]

One animation highlights different sides of the element by rotating
the light source around it. Its
[[svg/attributes/repeatCount|'''repeatCount''']] is set to
'''indefinite''', so after it proceeds from '''0''' to '''360'''
degrees, it restarts invisibly at '''0'''.

<syntaxhighlight lang="xml" highlight="8">
<animate
    id            = "lightAngleAnim"
    attributeName = "azimuth"
    from          = "0"
    to            = "360"
    begin         = "0s"
    dur           = "7s"
    repeatCount   = "indefinite"
    xlink:href    = "#lightAngleEffect"
/>
</syntaxhighlight>

A second un-synchronized animation raises and lowers the rounded
surface that makes the element appear beveled. Unlike the previous
animation, the [[svg/attributes/from|'''from''']] and
[[svg/attributes/to|'''to''']] values match, and the oscillation
occurs within the intervening frames defined in the
[[svg/attributes/values|'''values''']] attribute. (Unlike
[[tutorials/css_animations|CSS keyframe animations]], SVG does not
allow you to oscillate between the start and end values each time the
animation repeats.)

<syntaxhighlight lang="xml" highlight="4-5,8-9">
<animate
    id            = "elevationAnim"
    attributeName = "surfaceScale"
    from          = "5"
    to            = "5"
    begin         = "0s"
    dur           = "5s"
    values        = "5;20;5"
    repeatCount   = "indefinite"
    xlink:href    = "#elevationEffect"
/>
</syntaxhighlight>

(Yet another animation synchronizes with the first, repositioning the
shadow set by [[svg/elements/feOffset|'''feOffset''']] to match the
angle of the light source.)

[http://letmespellitoutforyou.com/samples/svg/filter_bevel.svg View this animation]

::'''Note:''' As of this writing, Firefox displays these animations in HTML content via the [[css/properties/filter|'''filter''']] CSS property along with the [[css/functions/url|'''url()''']] function.  See [[svg/tutorials/smarter_svg_filters|SVG Filters]] for more information on how to do this. However, there is no clear way to restart these animations when re-applying the filter in the HTML, so it is more appropriate for animations that execute continuously. As a workaround within SVG, toggle CSS classes to apply filters, then use a DOM mutation event such as '''begin = "0s;targetID.DOMAttrModified"''' to restart the animation.

You can set [[svg/attributes/repeatCount|'''repeatCount''']] to any
positive integer.  Each time an animation repeats, it produces a
[[dom/events/repeat|'''repeat''']] event, which you can also use to
synchronize other animations. The second example below runs it only
the first time the animation repeats:

 begin = "otherAnim.repeat"
 begin = "otherAnim.repeat(1)"

<div style="float:right;margin:10px">

[[Image:scr_svg_eyes.png]]

</div>

Each animation defines a potentially expansive length of time, over
which you can repeat an animation using a series of
[[svg/attributes/begin|'''begin''']] values. For example, the eyeballs
discussed in the [[svg/tutorials/smarter_svg_overview|SVG grand tour]]
blink several times in a row, leaving long pauses between each
iteration:

 begin = "4s;6s;8s;9s;11.5s;13s"

==Building progressions==

In all of these examples, the [[svg/attributes/from|'''from''']] and
[[svg/attributes/to|'''to''']] are fixed at specific values. Sometimes
it's useful to build on a value that results from a previous
animation.  Here's an example that moves a piece across an checker
board.

<syntaxhighlight lang="xml" highlight="">
<rect id="board" x="0" y="0" width="800" height="800" stroke="#000" stroke-width="6" fill="url(#chessBoard)"/>
<circle id="piece" fill="red" cx="150" cy="550" r="40"/>
</syntaxhighlight>

The board is defined as an 800&times;800 square, and the piece is
positioned over one of those squares. The accompanying animation moves
the piece over three squares to the right:

<div style="display:inline-block;width:45%">

[[Image:svga_checkerStart.png|300px]]

</div>

<div style="display:inline-block;width:45%">

[[Image:svga_checkerEnd.png|300px]]

</div>

<syntaxhighlight lang="xml" highlight="4,5,8,11-13">
<animate
    id            = "moveRight"
    attributeName = "cx"
    from          = "0"
    to            = "100"
    values        = "0;100;100"
    keyTimes      = "0;.7;1"
    begin         = "piece.click"
    dur           = "0.5s"
    fill          = "freeze"
    repeatCount   = "3"
    additive      = "sum"
    accumulate    = "sum"
    xlink:href    = "#piece"
/>
</syntaxhighlight>

When you set the [[svg/attributes/additive|'''additive''']] attribute
to '''sum''', the [[svg/attributes/from|'''from''']] and
[[svg/attributes/to|'''to''']] values are interpreted in terms
relative to the element's original value. In this case, the circle's
[[svg/attributes/cx|'''cx''']] is 150, so the animation starts there
and ends at that value plus 100, or 250.

When you set the [[svg/attributes/accumulate|'''accumulate''']]
attribute to '''sum''', each of the animation's repetitions build upon
the previous value. In this case, it proceeds from 150 to 250, 350,
then 450.

Notice also that the [[svg/attributes/begin|'''begin''']] does not
specify a time value, but instead responds when users click on the
piece. SVG supports interactive mouse, focus, and DOM mutation events.

[http://letmespellitoutforyou.com/samples/svg/anim_chess.svg View this animation]

==Curved motions==

The example above moves the game piece in a straight line, but instead
you can move it along the curve of a path. SVG provides an alternative
[[svg/elements/animateMotion|'''animateMotion''']] whose
[[svg/attributes/path|'''path''']] attribute specifies the movement
relative to its current position. The animation also specifies the the
graphic that is to be moved along that path.  This example moves the
game piece along the highlighted series of arcs, ''exactly'' as shown.
It relies on the ''A'' path command to define curves to destination
points up and to the right.

<syntaxhighlight lang="xml" highlight="4,8">
<defs>
<animateMotion
    id         = "animDiag"
    xlink:href = "#piece"
    begin      = "piece.click"
    fill       = "freeze"
    dur        = "3s"
    path       = "M 0,0 A 1,1 0 0 1 100,-100 A 1,1 0 0 1 200,-200 A 1,1 0 0 1 300,-300"
/>
</defs>
<rect id="board" x="0" y="0" width="800" height="800" stroke="#000" stroke-width="6" fill="url(#chessBoard)"/>
<circle id="piece" fill="red" cx="150" cy="550" r="40"/>
</syntaxhighlight>

<div style="display:inline-block">
[[Image:svga_motionChessBefore.png|300px]]
</div>
<div style="display:inline-block">
[[Image:svga_motionChessAfter.png|300px]]
</div>

[http://letmespellitoutforyou.com/samples/svg/anim_chessMotion.svg View this animation]

As an alternative, nesting an [[svg/elements/mpath|'''mpath''']]
element within the [[svg/elements/animateMotion|'''animateMotion''']]
makes the graphic travel along the contours of any referenced path.
This example makes an icon travel continuously in a around an
irregularly curved shape. The direction of movement depends on the
sequence of path commands, which in this case results in a
counter-clockwise motion:

<syntaxhighlight lang="xml" highlight="3,4,9">
<defs>
<animateMotion
    xlink:href  = "#icon"
    rotate      = "auto"
    start       = "0s"
    dur         = "10s"
    repeatCount = "indefinite"
>
    <mpath xlink:href="#shape"/>
</animateMotion>
</defs>
<image id="icon" x="0" y="0" width="50" height="50" xlink:href="icon.png"/>
<path id="shape" d="M 115,169 S 149,424 460,555 S 608,367 568,157 S 438,108 174,57 S 97,90 115,169"/>
</syntaxhighlight>

By default, the graphic retains its original orientation, as shown
below on the left where the icon points right. Specifying a
[[svg/attributes/rotate|'''rotate''']] attribute of '''auto''' keeps
it pointed in the direction of travel. A value of '''auto-reverse'''
makes the left side of graphic face forwards, and on the other side of
the path.

<div style="display:inline-block">
 rotate="0" (default)
[[Image:svga_motionZero.png|300px]]
</div>
<div style="display:inline-block">
 rotate="auto"
[[Image:svga_motionAuto.png|300px]]
</div>
<div style="display:inline-block">
 rotate="auto-reverse"
[[Image:svga_motionAutoReverse.png|300px]]
</div>

[http://letmespellitoutforyou.com/samples/svg/anim_motion.svg View this animation].
It additionally morphs the shape along which the icon travels.

To move text along a path, you need to use the
[[svg/elements/animate|'''animate''']] element, modifying the
[[svg/elements/textPath|'''textPath''']]'s
[[svg/attributes/startOffset|'''startOffset''']] attribute, which sets
the text's starting point relative to the start of the path.  In this
example, both offsets place the text out of view.  Ordinarily you can
specify percentages as offset values, but this example specifies units
relative to an arbitrary
[[svg/attributes/pathLength|'''pathLength''']] value, which helps to
pace the animation regardless of the path's actual length:

<syntaxhighlight lang="xml" highlight="4-6,13,20">
<defs>
<animate
   xlink:href    = "#txtPath"
   attributeName = "startOffset"
   from          = "1000"
   to            = "-1000"
   start         = "0s"
   dur           = "8s"
   repeatCount   = "indefinite"
/>
</defs>
<text id="txt">
  <textPath id="txtPath" xlink:href="#shape" startOffset="0">
    Moving text along a path
  </textPath>
</text>
<path
   id         = "shape"
   d          = "M 100,300 A 1,1 0 0 1 500,300"
   pathLength = "1000"
   />
</syntaxhighlight>

[[Image:svga_motionText.png]]

[http://letmespellitoutforyou.com/samples/svg/anim_motionText.svg View this animation]

==Animating transforms==

Since transform values can specify a combination of functions, you
need to use the alternative
[[svg/elements/animateTransform|'''animateTransform''']] element to
clarify what is being animated. The additional
[[svg/attributes/type|'''type''']] attribute specifies the transform
function to be animated.  This example moves a graphic diagonally:

<syntaxhighlight lang="xml" highlight="3">
<animateTransform
   attributeName = "transform"
   type          = "translate"
   from          = "0,0"
   to            = "10,10"
   begin         = "0s"
   dur           = "1s"
   xlink:href    = "#shiftDiagonal"
/>
</syntaxhighlight>

The element to be animated must not specify other transforms.  If you
want to animate the rotation in the example on the left below, you
need to split out the translation into a different element as shown on
the right:

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<g transform="translate(10,10) rotate(-90)">
  <use xlink:href="#tileSquare" />
</g>
</syntaxhighlight>

</div>

<div style="display:inline-block">

<syntaxhighlight lang="xml">
<g transform="translate(10,10)">
  <g id="pivot" transform="rotate(-90)">
    <use xlink:href="#tileSquare" />
  </g>
</g>
</syntaxhighlight>

</div>

[http://letmespellitoutforyou.com/samples/svg/anim_transform.svg View this animation]
for an example of transforms on elements within a pattern. As of this
writing, animating transforms on entire patterns
([[svg/attributes/patternTransform|'''patternTransform''']])
does not work reliably in many browsers.

<div style="float:right">

[[Image:svga_transform.png|200px]]

</div>

<!--

brain example

==Color and other properties==

___

* animateColor
* instead of via CSS?
* attributeType="CSS"
* "set" discrete values

==Scripting animations==

___

* beginElement()
* beginElementAt(tv)
* restart = whenNotActive
-->

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
|Topic_clusters=Animation
}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}