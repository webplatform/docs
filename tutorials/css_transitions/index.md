{{Page_Title|Dynamic visual effects with CSS3 transitions}}
{{Flags
|High-level issues=Stub
|Editorial notes=[[User:Sierra]] has content intended for this page. See bug [https://www.w3.org/Bugs/Public/show_bug.cgi?id=20410 #20410]
}}
{{Byline}}
{{Summary_Section|CSS transitions offer the easiest way to animate an
interface.  CSS is used everywhere to control how web pages appear,
and shifts from one set of style sheets to another ordinarily occur
abruptly.  Adding transition properties allows most of those changes
to occur gradually, for a more vibrant, fluid interface.
}}
{{Tutorial
|Content=

This tutorial introduces CSS's various transition properties and shows
you how to control how smoothly transitions execute. It shows you how
to create sequences of more than one transition, but increasingly
complex movements require [[tutorials/css_animations|keyframe
animations]], which work similarly.  You should become familiar with
what CSS ''transitions'' can do before mastering ''animations''.  Both
kinds of CSS-based animation require none of the JavaScript timers
traditionally used to move things around, and they execute much
faster.

While transitions allow you to apply hover effects and other
relatively marginal enhancements to traditional desktop interfaces,
they are particularly useful for small-screen mobile interfaces in
which displaying elements need to slide or fade out of view, or else
collapse into icons.  The examples below introduce broadly useful
techniques, but focus on opportunities where transitions can drive a
mobile interface.

==The transition property==

For transitions to work, there need to be two sets of style sheets
that might apply to any element as users interact with the page. In
this case, tapping a small '''nav''' element expands it out to a wider
navigation panel:

[[Image:transit_parent.png]]

To achieve this effect, a default style sheet defines most of how it
appears. A second style sheet changes how it appears when it is
assigned the ''expanded'' class.

 nav {
         /* transition applies to all varying elements */
     transition            : all 0.5s;
         /* dimensions and position (mostly outside view) */
     height                : 42px;
     width                 : 300px;
     position              : absolute;
     right                 : -260px;
     top                   : 10px;
     padding               : 2px;
     overflow              : hidden;
     box-sizing            : border-box;
         /* define icon */
     background-image      : url(html5.png);
     background-position-x : left;
     background-position-y : 50%;
     background-repeat     : no-repeat;
     background-size       : contain;
     background-color      : #fff;
         /* border and shadow hidden by default */
     border                : transparent solid medium;
     border-radius         : 4px;
     box-shadow            : 0 0 1em transparent;
 }
 nav.expanded  {
         /* transition applies to these varying elements */
     right                 : 10px;   /* bring panel into view */
     background-position-x : 400px;  /* icon out of view */
     border                : #aaa solid medium; 
     box-shadow            : 0 0 1em #777;
 }

The ''expanded'' class specifies a handful of CSS properties that
override those that apply without the class.  Adding the
'''transition''' property makes those properties animate when toggling
the ''expanded'' class:

 transition         : all 0.5s;
 -moz-transition    : all 0.5s;
 -o-transition      : all 0.5s;
 -webkit-transition : all 0.5s;

Changes to the values of the '''right''' and '''background-position'''
properties makes the element and its displaying icon slide in from the
right. As it does, the border and shadow appear and get darker.

'''Note:''' Transition properties were implemented recent enough that
many browser engines only support them with ''vendor prefixes'' such
as '''-moz-''', '''-o-''', or '''-webkit-''' as shown above. Further
examples only show un-prefixed transition property names, but for
widest support you should apply all of them.

The '''transition''' property specifies which properties to animate,
'''all''' in this case, and how long the animation takes to execute.
It is shorthand for these separate properties:

 transition-property : all;
 transition-duration : 0.5s;
 transition-duration : 500ms; /* same as above, but expressed as milliseconds */

To see the animation in action, all you need is a mechanism to apply
the ''expanded'' class, in this case a '''click''' handler that also
responds to touch input:

 document.querySelector('nav').addEventListener('click', function(event) {
     event.currentTarget.classList.toggle('expanded');
 });

==Parallel transitions==

We want the panel to display a set of nested navigation icons, in this
case a set of horizontal '''div''' elements. A second '''transition'''
property animates these nested elements depending on the state of their
parent '''nav''' element:

 nav > div {
     transition        : all 0.5s;
     height            : 34px;
     width             : 34px;
     background-size   : contain;
     display           : inline-block; /* arranged horizontally */
     opacity           : 0;            /* faded */
     transform         : scale(0);     /* scaled down */
 }
 nav.expanded > div {
     opacity           : 1;
     transform         : scale(1);
 }

The animation fades the icons, and grows or shrinks them down to a
point. (See the [[tutorials/css_transforms|transforms tutorial]] for
more information.) Combined, the two sets of transitions appear like
this:

[[Image:transit_simple.png|280px]]

==Transitional sequences==

[[Image:transit_sequence.png|800px]]

<!--
NOTE: UNFINISHED. DO NOT EDIT.

* multiple transitions
* P delay: 
* bidirectional
-->

==Timing functions==

<!--
* P timing
* curves, keyword shorthands
* steps
-->

==The transitionend event==

<!--
* example: self-dismissing panel
* TIP: spurious transitions as alternative to setTimeout
-->

==Cross-fades, filters, and other exotic effects==

<!--
* default cross-fade for background image?
* cross-fade() function
* hue-rotate
-->

==What can be transitioned==

<!--
* NO generated ::before & ::after
* NO discrete values
* NO mismatching parameters
* gradients?
* numeric
* color
-->

}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=4.0
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=4.0
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=Yes
|Opera_prefixed_version=10.5
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=3.1
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Yes
|Android_prefixed_version=2.1
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Yes
|Firefox_mobile_prefixed_version=15.0
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Yes
|Opera_mobile_prefixed_version=10.0
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Yes
|Safari_mobile_prefixed_version=3.2
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Transistions
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}