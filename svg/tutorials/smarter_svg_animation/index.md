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

[[Image:svga_simpleSwipe.png]]

<!--

(e.g. swipe effect)

* begin = timecount (s/ms)
* dur
* from
* to

* attributeName="???"
* attributeType="xml"

<syntaxhighlight lang="xml">
<text id="TXT" x="0" y="100"> An SVG Animation
    <animate
        id            = "swipe"
        attributeType = "XML"
        attributeName = "x"
        calcMode      = "discrete"
        keyTimes      = "0;0.2;0.4;0.6;0.8;1"
        values        = "1000;800;600;400;200;0"
        begin         = "0s;TXT.click"
        dur           = "10s"
        from          = "1000"
        to            = "0"
    />
</text>
</syntaxhighlight>

==Sequences==

(e.g. oscillating blur)

* values (abs)
* values (%)

* "values" along the way; e.g. oscillation
* "keyTimes" matches "values"

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