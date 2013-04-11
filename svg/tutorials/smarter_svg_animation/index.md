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

Instead of nesting the animation, you can also link the element you
want to animate indirectly. However, the animation can only be applied
to a single element, so there's no real difference:

<syntaxhighlight lang="xml">
<defs>
<animate id="swipeAnim" xlink:href="#swipeText" attributeName="x"
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

==A sequence of values==

This animation swipes in, but then comes to an abrupt stop.  This more
natural-looking variation bounces the text a bit off the left wall:

<syntaxhighlight lang="xml" highlight="9-10">
<animate
    id            = "swipe"
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

The [[svg/attributes/values|'''values''']] attribute uses semicolons
to specify a series of intermediate values between the animation's
[[svg/attributes/begin|'''begin''']] and
[[svg/attributes/end|'''end''']] points. Starting at '''1000''', the
animation proceeds to the '''0''' point that represents the left wall,
then goes a bit further to '''-20''', then back to '''10''' before
finally settling at '''0'''.

Without the accompaying [[svg/attributes/keyTimes|'''keyTimes''']],
the animation still looks awkward. The initial transition between
'''1000''' and '''0''' executes ''very'' quickly, after which the
subsequent transitions seem too slow. The fixes this by
[[svg/attributes/keyTimes|'''keyTimes''']] specifying the share of
time, between 0 and 1, each segment should take to execute. In this
case, the initial transition that slides in the text takes 80% of the
total duration. (Otherwise, with five values the default would be a
far more brisk 25%.) The number of
[[svg/attributes/keyTimes|'''keyTimes''']] must match the number of
[[svg/attributes/values|'''values''']], or the animation does not
work.

<!--

[[svg/attributes/foo|'''foo''']]

==Setting the pace==

(swipe + bounce)

* calcMode = discrete: like CSS step()
* calcMode = linear (default) between values
* calcMode = paced (linear over entire animation; ignoring intermedite values)
* calcMode = spline

* "keySplines" == CSS cubic-bezier()

==Syncronization==

* begin = id.event
* begin = id.event+timeValue
* circle-anim.repeat(1) + 2.5s
* prev.begin

==Repetition, Repetition

* begin (>1) re-fires (eyeballs)
* repeatCount = "indefinite"/###
* fill = freeze (like fill-mode)

==Building progressions==



* from/by???
* additive="sum" == relative "from" values
* accumulate="sum" == build on prior values

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