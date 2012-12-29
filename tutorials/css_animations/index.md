{{Page_Title|Making things move with CSS3 animations}}
{{Flags
|High-level issues=Stub
|Editorial notes=[[User:Sierra]] has content intended for this page. See bug [https://www.w3.org/Bugs/Public/show_bug.cgi?id=20410 #20410]
}}
{{Byline}}
{{Summary_Section|CSS animations allow you to build complex animated
sequences.  Like [[tutorials/css_transitions|transitions]], they
manipulate the CSS properties that control how interface elements
appear. Unlike transitions, they are not tied to shifts between style
sheets that distinguish interface states.  Keyframe animations can
execute freely, and offer the best way to build complex effects into
an interface.
}}
{{Tutorial
|Content=

To get the most from this tutorial, you should already be familiar
with [[tutorials/css_transitions|CSS transitions]].  Since they work
similarly, the term ''CSS animations'' often serves as a shorthand to
refer to transitions as well, but this tutorial only discusses
''keyframe animations''.

==Animation properties==

To understand how animations work, start with a simple example of a
pulsing icon, which may be used in a mobile interface to indicate what
part of an application is selected. The animation continuously shrinks
and grows the icon as it dims and brightens it:

[[Image:anim_pulse.png]]

The [[css/properties/animation|'''animation''']] CSS property
specifies the ''name'' of an animation you will supply, '''pulse''' in
this case, and its overall ''duration'' of 1 second. Both are
required:

 div.selected {
     animation : pulse 1s infinite;
 }

The '''infinite''' keyword indicates that the animation repeats
indefinitely. If not specified, the animation executes only once.

The [[css/properties/animation|'''animation''']] property is a
shorthand that combines the values of others:

 div.selected {
     animation-name            : pulse;
     animation-duration        : 1s;
     animation-iteration-count : infinite;
 }

Animation properties are standard in many browsers, but as of this
writing require prefixes for WebKit browsers and older versions of
Gecko and Opera. For widest support, you should define animation
properties redundantly:

 div.selected {
     -webkit-animation : pulse 1s infinite;
     -moz-animation    : pulse 1s infinite;
     -o-animation      : pulse 1s infinite;
     animation         : pulse 1s infinite;
 }

From here on, examples feature only the un-prefixed property names.

==The @keyframes rule==

The [[css/properties/animation-name|'''animation-name''']] property
specifies an animation named '''pulse'''. Use a
[[css/atrules/@keyframes|'''@keyframes'''] rule within the CSS to
define each named animation sequence:

 @keyframes pulse {
     from { 
         transform : scale(1);
         opacity   : 1;
     }
     50% { 
         transform : scale(0.75);
         opacity   : 0.25;
     }
     to { 
         transform : scale(1);
         opacity   : 1;
     }
 }

The entire sequence between '''from''' and '''to''' executes over the
span of time defined by the
[[css/properties/animation-duration|'''animation-duration''']]
property.  Each keyframe within the sequence behaves like a CSS
selector, manipulating the values of individual properties.
In this case, [[css/properties/opacity|'''opacity''']] dims the icon
and [[css/properties/transform|'''transform''']] shrinks it.  (See the
[[tutorials/css_transforms|tutorial on transforms]] for details on the
[[css/properties/transform|'''transform''']] property's '''scale()'''
function.)

Along with animation properties, each
[[css/atrules/@keyframes|'''@keyframes''']] rule also needs to be
prefixed to run on WebKit-based browsers:

 @-webkit-keyframes pulse {
    0%   { -webkit-transform: scale(1)   ; opacity: 1;    }
    50%  { -webkit-transform: scale(0.75); opacity: 0.25; }
    100% { -webkit-transform: scale(1)   ; opacity: 1;    }
 }

This example also substitutes '''0%''' and '''100%''' for their
synonymous keywords '''from''' and '''to'''.

==Alternation==

...

<!--
* [[css/properties/animation-direction|'''animation-direction''']]
* iteration-count
* direction
* from/to
* EXAMPLE: pulse icon using direction/iteration
-->

==Multiple animations==

...

<!--
[[css/properties/animation-delay|'''animation-delay''']]
* simultaneous for different elements
* multiple for an element
* EXAMPLE: pulse opacity and scale transform
* can't animate (or transition) the same property at the same time
* EXAMPLE: insertBanner, then cycleBanner
-->

==Fill mode==

...

<!--
* [[css/properties/animation-fill-mode|'''animation-fill-mode''']]
* animations override style sheets
* fill-mode overrides prior to or following animation's execution
* EXAMPLE: insertBanner persists after executing
-->

==Timing functions==

...

<!--
[[css/properties/animation-timing-function|'''animation-timing-function''']]
* same as for transitions
* can change function mid-execution
* EXAMPLE: skew transform slide-in panels
-->

==Dynamic keyframes==

...

<!--
* [[css/properties/animation-play-state|'''animation-play-state''']]
* inject into style element, scoped or otherwise...
* ...or programmatically

[[css/properties/animation-iteration-count|'''animation-iteration-count''']]


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
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}