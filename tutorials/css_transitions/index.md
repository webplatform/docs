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
[[css/properties/transition|'''transition''']] property makes those
properties animate when toggling the ''expanded'' class:

 transition         : all 0.5s;
 -moz-transition    : all 0.5s;
 -o-transition      : all 0.5s;
 -webkit-transition : all 0.5s;

Changes to the values of the [[css/properties/right|'''right''']] and
[[css/properties/background-position|'''background-position''']]
properties makes the element and its displaying icon slide in from the
right. As it does, the border and shadow appear and get darker.

'''Note:''' Transition properties were implemented recent enough that
many browser engines only support them with ''vendor prefixes'' such
as '''-moz-''', '''-o-''', or '''-webkit-''' as shown above. Further
examples only show un-prefixed transition property names, but for
widest support you should apply all of them.

The [[css/properties/transition|'''transition''']] property specifies
which properties to animate, '''all''' in this case, and the half
second the animation takes to execute.  It is shorthand for these
separate properties:

 transition-property : all;
 transition-duration : 0.5s;
 transition-duration : 500ms; /* same as above, but expressed as milliseconds */

To see the animation in action, all you need is a mechanism to apply
the ''expanded'' class, in this case a '''click''' handler that also
responds to touch input:

 document.querySelector('nav').addEventListener('click', function(event) {
     event.currentTarget.classList.toggle('expanded');
 });

You'll notice that transitions respond very gracefully by reversing
direction if you re-toggle the class while the animation is executing.

==Parallel transitions==

We want the panel to display a set of nested navigation icons, in this
case a set of horizontal '''div''' elements. A second
[[css/properties/transition|'''transition''']] property animates these
nested elements depending on the state of their parent '''nav'''
element:

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

The [[css/properties/opacity|'''opacity''']] property fades the icons,
and [[css/properties/transform|'''transform''']] grows or shrinks them
down to a point. (See the [[tutorials/css_transforms|tutorial on
CSS transforms]] for details.)  Combined, the two sets of transitions
execute simultaneously:

[[Image:transit_simple.png|280px]]

==Sequential transitions==

You are not limited to a single set of transitions to get from one set
of style sheets to another. The panel in this example first grows to
its full width, then lengthens. The sequence is then reversed when
collapsing the panel back down to icon size:

[[Image:transit_sequence.png|900px]]

Here is the relevant CSS:

 div {
     width               : 56px;
     height              : 56px;
     transition-property : height , width;  /* collapse sequence */
     transition-duration : 0.5s   , 0.5s;
     transition-delay    : 0.0s   , 0.5s;   /* delay 2nd transition */
 }
 div.expanded {
     transition-property : width  , height; /* expand sequence */
     width               : 280px;
     height              : 400px;
 }

Each transition property uses commas to delimit additional transitions
that form the larger second-long sequence. In this case, the duration
for each is the same: half a second. The
[[css/properties/transition-delay|'''transition-delay''']] property
specifies that the first executes immediately, but the second waits
until the first is complete.

This example also specifies individual property names rather than
'''all'''. When transitioning to the ''expanded'' class, the
[[css/properties/width|'''width''']] animates before the
[[css/properties/height|'''height''']], and the sequence reverses in
the other direction.

The [[css/properties/transition|'''transition''']] shorthand property
also accommodates additional transitions. Here is the same as above,
but expressed more tersely:

 div          { transition: height 0.5s 0.0s , width  0.5s 0.5s ; }
 div.expanded { transition: width  0.5s 0.0s , height 0.5s 0.5s ; }

The first supplied time value is interpreted as the
[[css/properties/transition-duration|'''transition-duration''']], and the second as the
[[css/properties/transition-delay|'''transition-delay''']].

Note that with no delay specified, you can use more than one
transition to animate selected properties simultaneously, which might
be useful if you want to animate some properties but not '''all''' of
them. You can also stagger the delays so that execution overlaps.  In
this example, a single transition specifies the
[[css/properties/transform|'''transform''']] property to move six
cards to the right over the course of one second, but the delay for
each is successively staggered up to half a second so that the overall
sequence takes 1.5 seconds to execute:

 section > div {
     transition: transform 1s;
     transform: translateX(0px);
     /* ^^^ this transform is optional, otherwise transition assumes default value */
 }
 section.deal > div {
     transform: translateX(300px); /* move to right */
 }
 section > div:nth-of-type(6) {
     transition-delay: 0.0s;
     background-image: url(QueenSpade.png);
 }
 section > div:nth-of-type(5) {
     transition-delay: 0.1s;
     background-image: url(KingClub.jpeg);
 }
 section > div:nth-of-type(4) {
     transition-delay: 0.2s;
     background-image: url(JackClub.jpeg);
 }
 section > div:nth-of-type(3) {
     transition-delay: 0.3s;
     background-image: url(AceSpade.jpeg);
 }
 section > div:nth-of-type(2) {
     transition-delay: 0.4s;
     background-image: url(JackSpade.jpeg);
 }
 section > div:nth-of-type(1) {
     transition-delay: 0.5s;
     background-image: url(JackHeart.jpeg);
 }

The overall movement is staggered like this:

[[Image:transit_delay.png]]

==Timing functions==

You may notice in the example above that the cards are not evenly
spaced. That's because transitions by default start out slowly, gather
speed, then slow down again at the end.  The
[[css/properties/transition-timing-function|'''transition-timing-function''']]
property specifies this behavior. By default it uses an '''ease'''
value. If it were '''linear''', they would all start and stop abruptly
and move at the same speed:

[[Image:transit_linear.png]]

Browsers represent these keywords as bezier curves, which makes their
response easier to visualize.  Here is the basic set of keyword values
along with their alternate '''cubic-bezier()''' functions.  The
animation's elapsed time and progress correspond to ''x'' and ''y''
axes, so the more the line curves vertically along the way, the faster
it moves:

* '''ease''': '''cubic-bezier(0.25, 0.1, 0.25, 1.0)'''
[[Image:transitF_ease.png]]

* '''ease-in-out''': '''cubic-bezier(0.42, 0, 0.58, 1.0)'''
[[Image:transitF_easeinout.png]]

* '''ease-in''': '''cubic-bezier(0.42, 0, 1.0, 1.0)'''
[[Image:transitF_easein.png]]

* '''ease-out''': '''cubic-bezier(0, 0, 0.58, 1.0)'''
[[Image:transitF_easeout.png]]

* '''linear''': '''cubic-bezier(0.0, 0.0, 1.0, 1.0)'''
[[Image:transitF_linear.png]]

This useful [http://cssglue.com/cubic cubic bezier function utility]
allows you to create your own custom curve and the see the result
applied to various animations.

Timing functions can also be specified as part of the
[[css/properties/transition|'''transition''']] shorthand
property. This example makes a sequence of two '''ease-in''' and
'''ease-out''' transitions resemble the behavior of a single
'''ease-in-out''' function:

 div          { transition: height 0.5s 0.0s ease-in, width  0.5s 0.5s ease-out; }
 div.expanded { transition: width  0.5s 0.0s ease-in, height 0.5s 0.5s ease-out; }

As an alternative to response curves, the '''steps()''' function
specifies a series of distinct frames with no smoothing applied. This
animates three interim steps that occur between the start and end
points:

 transition-timing-function : steps(5);


<!--
NOTE: UNFINISHED. DO NOT EDIT.
==The transitionend event==
* example: self-dismissing panel
* TIP: spurious transitions as alternative to setTimeout
-->

<!--
==Cross-fades, filters, and other exotic effects==
* default cross-fade for background image or cross-fade() function?
* hue-rotate & other filters
* gradients?
-->

<!--
==What can be transitioned==
* NO generated ::before & ::after
* NO discrete values
* NO mismatching parameters (polygon, gradient stops)
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