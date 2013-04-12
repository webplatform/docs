{{Page_Title|SVG animation and interaction}}
{{Flags
|High-level issues=Stub
|Checked_Out=Yes
|Editorial notes=[new content edited offline by Sierra ([[User:Sierra|Sierra]] ([[User talk:Sierra|talk]])); please do not edit]
}}
{{Byline}}
{{Summary_Section|This guide shows you how to use SVG animation, comparing it with CSS techniques. It shows how to control SVG animations from JavaScript, and details other interaction features native to SVG.}}
{{Tutorial
|Content=

Interfaces become more vibrant once you add animation effects.  This
guide focuses on SVG's built-in animation features, which derive from
SMIL, the ''Synchronized Multimedia Integration Language''.  As
discussed in the [[svg/tutorials/smarter_svg_overview|SVG grand
tour]], some SVG element attributes are actually implemented as CSS
''properties'', and thus respond to CSS
[[tutorials/css_transitions|transitions]] and
[[tutorials/css_animations|keyframe animations]]. The techniques
described here offer the only way to animate SVG ''attributes'', but
they can be used for ''properties'' as well. You'll also learn how to
dynamically modify any attribute values that can't be animated.

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

==Delaying the animation==

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

==A sequence of frames==

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

==Animation sequences==

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
axis. But note the animation's [[svg/attributes/begin|'''begin''']]
attribute no longer specifies a time value. Instead, this animation
begins whenever the previous one ends:

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

==Setting the pace==

Instead of bouncing the text off the wall, this variation brings it to
a more gradual stop:

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

By default, the [[svg/attributes/calcMode|'''calcMode''']] is
'''linear''', which makes the action proceed in a straight line.
Setting it to '''spline''' makes it respond to a bezier curve, defined
by the value of [[svg/attributes/keySplines|'''keySplines''']]. You
can use semicolons to specify as many curves as there are frames in
your animation.

The following examples show how these response curves behave.  Each
''x'' axis represents the animation's elapsed time, and the ''y'' axis
represents its progress, so the more the line curves vertically along
the way, the faster the animation proceeds at that point.

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

==Repetition, repetition, repet...==

The examples above all execute once, but this example uses
[[svg/attributes/repeatCount|'''repeatCount''']] to animate
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

<div style="display:inline-block;max-width:45%">

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

</div>

<div style="display:inline-block;max-width:45%">

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

</div>

::'''Note:''' As of this writing, Firefox displays these animations in HTML content via the [[css/properties/filter|'''filter''']] CSS property along with the [[css/functions/url|'''url()''']] function to specify the SVG filter.  See [[svg/tutorials/smarter_svg_filters|SVG Filters]] for more information on how to do this. However, there is no clear way to restart these animations when re-applying the filter in the HTML, so it is more appropriate for animations that execute continuously. 

You can set [[svg/attributes/repeatCount|'''repeatCount''']] to any
positive integer.  Each time an animation repeats, it produces a
[[dom/events/repeat|'''repeat''']] event, which you can also use to
synchronize other animations. The second example below runs it only
the first time the animation repeats:

 begin = "otherAnim.repeat"
 begin = "otherAnim.repeat(1)"

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

When you set the [[svg/attributes/additive|'''additive''']] attribute
to '''sum''', the [[svg/attributes/from|'''from''']] and
[[svg/attributes/to|'''to''']] values are interpreted relative to the
element's original value. In this case, the circle's
[[svg/attributes/cx|'''cx''']] is 150, so the animation starts there
and ends at that value plus 100, or 250.

When you set the [[svg/attributes/accumulate|'''accumulate''']]
attribute to '''sum''', each of the animation's repetitions build upon
the previous value. In this case, it proceeds from 150 to 250, 350,
then 450.

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


<!--

* from/by???
* additive="sum" == relative "from" values
* accumulate="sum" == build on prior values

[[svg/attributes/foo|'''foo''']]
[[svg/tutorials/smarter_svg_overview|SVG grand tour]]

[[Image:scr_svg_eyes.png]]


* begin (>1) re-fires (eyeballs)
* repeatCount = "indefinite"/###





<syntaxhighlight lang="xml" highlight="">
</syntaxhighlight>

==Scripting animations==

* restart = whenNotActive
* begin/repeat/end events

* beginElement()
* beginElementAt(tv)

pause

==Animating properties==

* instead of via CSS?

==Specialized animation types==

* animateMotion (move along moving path?)
** rotate="auto" (default)
** rotate="auto-reverse" invert
** path="data" vs mpath

* animateColor

* animateTransform (brain)

==The 'set' shorthand==

* discrete values

===___===

* begin = timecount (s/ms)

* attributeType="xml"

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