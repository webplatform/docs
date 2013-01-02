{{Page_Title|Making things move with CSS3 animations}}
{{Flags
|High-level issues=Stub
|Editorial notes=[[User:Sierra]] has content intended for this page. See bug [https://www.w3.org/Bugs/Public/show_bug.cgi?id=20410 #20410]
}}
{{Byline}}
{{Summary_Section|CSS animations allow you to build complex animated
sequences. Like [[tutorials/css_transitions|transitions]], they
manipulate the CSS properties that control how interface elements
appear. Unlike transitions, they are not tied to shifts between style
sheets that distinguish interface states. Keyframe animations can
execute freely, and offer the best way to build complex effects into
an interface.
}}
{{Tutorial
|Content=

To get the most from this tutorial, you should already be familiar
with [[tutorials/css_transitions|CSS transitions]]. Since they work
similarly, the term ''CSS animations'' often serves as a shorthand to
refer to transitions as well, but this tutorial only discusses
''keyframe animations''.

==Animation properties==

To understand how animations work, start with an example of a pulsing
icon, which may be used in a mobile interface to indicate what part of
an application is selected. The animation continuously shrinks and
grows one of the icons as it dims and brightens it. This simple
example will illustrate several other features below:

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
writing require prefixes for all WebKit browsers and older versions of
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
[[css/atrules/@keyframes|'''@keyframes''']] rule within the CSS to
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
property. Each keyframe within the sequence behaves like a CSS
selector, manipulating the values of individual properties.
In this case, [[css/properties/opacity|'''opacity''']] dims the icon
and [[css/properties/transform|'''transform''']] shrinks it. (See the
[[tutorials/css_transforms|tutorial on transforms]] for details on the
[[css/properties/transform|'''transform''']] property's '''scale()'''
function.)

As with animation properties, each
[[css/atrules/@keyframes|'''@keyframes''']] rule also needs to be
prefixed redundantly to run on WebKit-based browsers such as Chrome
and Safari. The transform properties below are also prefixed:

 @-webkit-keyframes pulse {
    0%   { -webkit-transform: scale(1)   ; opacity: 1;    }
    50%  { -webkit-transform: scale(0.75); opacity: 0.25; }
    100% { -webkit-transform: scale(1)   ; opacity: 1;    }
 }

This example also substitutes '''0%''' and '''100%''' for their
synonymous keywords '''from''' and '''to'''.

==Changing Direction==

This simple animation can also be alternated to produce the same effect:

 div.selected {
     animation-name            : pulse;
     animation-duration        : 0.5s;
     animation-iteration-count : infinite;
     animation-direction       : alternate;
 }

The [[css/properties/animation-duration|'''animation-duration''']] is
now half of its previous value. Setting
[[css/properties/animation-direction|'''animation-direction''']] to
'''alternate''' makes the animation execute in normal order
('''from'''/'''to'''), then in reverse order ('''to'''/'''from''') for
even-numbered iterations. This allows the animation's start and end
points to vary:

 @keyframes pulse {
    from { transform: scale(1)   ; opacity: 1;    }
    to   { transform: scale(0.75); opacity: 0.25; }
 }

(You can also set
[[css/properties/animation-direction|'''animation-direction''']] to
always '''reverse''', or to '''reverse-alternate'''.)

==Multiple animations==

Animation properties accept more than one comma-delineated value,
which allows you to chain together different animations or run them
concurrently.

This variation on the pulsing icon uses two keyframes to manipulate
the [[css/properties/opacity|'''opacity''']] and
[[css/properties/transform|'''transform''']] properties separately.
In this case, setting different durations makes the two ''fade'' and
''shrink'' effects fall out of phase:

 div.selected {
     animation: fade 0.5s infinite alternate, shrink 0.53s infinite alternate;
 }
 /* long form: */
 div.selected {
     animation-name            : fade      , shrink    ;
     animation-duration        : 0.5s      , 0.53s     ;
     animation-iteration-count : infinite  , infinite  ;
     animation-direction       : alternate , alternate ;
 }
 @keyframes fade {
     from { opacity   : 1; }
     to   { opacity   : 0.25; }
 }
 @keyframes shrink {
     from { transform : scale(1); }
     to   { transform : scale(0.75); }
 }

Make sure that any keyframes or transitions that execute concurrently
don't manipulate any of the same properties. This is ''not'' a problem
for animations or transitions applied to different elements.

==Setting a Delay==

As with transitions, animations can be delayed before they execute.
Use the [[css/properties/animation-delay|'''animation-delay''']]
property to wait some time before pulsing the icon:

 div.selected {
     animation-name            : pulse;
     animation-duration        : 0.5s;
     animation-iteration-count : 6;
     animation-direction       : alternate;
     animation-delay           : 3s;
 }

(In this version, the icon pulses three times.)

Whenever two time measurements are specified in a shorthand property
value, the second is interpreted as the delay:

 div.selected {
     animation : pulse 0.5s 3s infinite alternate;
 }

This more elaborate example shows a delayed animation within a mobile
interface. After an initial pause, content shifts down to make room
for a series of banner advertisements, which then continuously cycle
horizontally and rewind to display the first:

[[Image:anim_cycle.png]]

To achieve this effect, the
[[css/properties/animation-delay|'''animation-delay''']] property
makes content shift down after 4 seconds. Here is the relevant CSS:

 article {
     animation-name            : displaceContent;
     animation-duration        : 1s;
     animation-delay           : 4s;
     animation-iteration-count : 1;
     animation-fill-mode       : forwards;
 }
 @keyframes displaceContent {
     from { transform : translateY(0em) }
     to   { transform : translateY(3em) } /* slide down to make room for advertisements */
 }

The
[[css/properties/animation-iteration-count|'''animation-iteration-count''']]
property makes the animation execute only once. The next section
explains the
[[css/properties/animation-fill-mode|'''animation-fill-mode''']]
property.

The banner's first animation (''insertBanner'') closely mirrors that
of the content (''displaceContent'') shown above. After 4 seconds, it
slides into view from off the screen:

 header {
     animation-name            : insertBanner , scrollBanner;
     animation-duration        : 1s           , 25s;
     animation-delay           : 4s           , 5s;
     animation-iteration-count : 1            , infinite;
     animation-fill-mode       : backwards    , none;
     width                     : 500%;        /* wide banner featuring 5 panels */
     column-count              : 5;
     column-gap                : 0;
 }
 @keyframes insertBanner {
     from { transform : translateY(-6em) } /* slide down from off-screen */
     to   { transform : translateY(0em) }
 }

The banner's second animation (''scrollBanner'') takes over at the
5-second mark, after the first has completed. Over the course of 25
seconds, it shifts the banner sideways to view each advertisement for
nearly 5 seconds. After rewinding to its initial position 97% of the
way through the keyframes, setting
[[css/properties/animation-iteration-count|'''animation-iteration-count''']]
to '''infinite''' makes the animation replay indefinitely:

 @keyframes scrollBanner {
     from { transform : translateX(0) }
     17%  { transform : translateX(0%) }
     20%  { transform : translateX(-20%) }
     37%  { transform : translateX(-20%) }
     40%  { transform : translateX(-40%) }
     57%  { transform : translateX(-40%) }
     60%  { transform : translateX(-60%) }
     77%  { transform : translateX(-60%) }
     80%  { transform : translateX(-80%) }
     97%  { transform : translateX(-80%) }
     to   { transform : translateX(0%) }
 }

==Fill mode==

Each keyframe within an animation specifies CSS properties, just like
regular CSS selectors. Properties manipulated by keyframes may vary
from those defined or inherited by selectors. By default, after
animations complete their series of iterations, these properties
abruptly snap from the final keyframe's value back to their original
value. Likewise when animations are delayed, properties snap from
their original values to that of the first keyframe's value.

The [[css/properties/animation-fill-mode|'''animation-fill-mode''']]
property fixes this problem. Setting it to '''forwards''' makes the
final keyframe's property values persist after the animation
completes. Setting it to '''backwards''' makes the first keyframe's
property override how the property would appear without the
animation. Setting it to '''both''' makes the keyframe's properties
override the element's default properties both before and after the
animation executes. Setting it to the default value of '''none'''
keeps all properties at their default values unless the animation is
executing.

Note that none of these values make any difference for animations
whose [[css/properties/animation-delay|'''animation-delay''']] is set
to zero, and whose
[[css/properties/animation-iteration-count|'''animation-iteration-count''']]
is '''infinite'''. Even then, they only make a difference for
properties whose values specified at the start or end of the animation
vary from how they are already specified by the element itself.

The banner animation shown above gives an example of how to use
[[css/properties/animation-fill-mode|'''animation-fill-mode''']].  By
default, both the banner and the main content inhabit the same space
at the top of the screen. The content's ''displaceContent'' animation
slides it out of its default position, and its fill-mode of
'''forwards''' keeps it there after it is done sliding. If it didn't,
it would snap right back to the top of screen. Likewise, the banner's
''insertBanner'' animation slides it from a position specified in the
first keyframe, and its fill-mode of '''backwards''' keeps it there
before the delayed animation starts to execute, and it slides down to
its default position.

Fill mode can override not only an element's underlying properties,
but other animations as well.  For the banner's second animation, the
[[css/properties/animation-fill-mode|'''animation-fill-mode''']] is
set to '''none'''. If it were set to '''both''' or '''backwards''',
the first animation would not execute. Since animations are
interpreted in their order of declaration, and since both animations
manipulate the [[css/properties/transform|'''transform''']] property,
specifying a fill-mode for the period before the second animation
executes would override whatever the first animation does with the
'''transform''' property:

 header {
     /* both animations alter the 'transform' property: */
     animation-name            : insertBanner     , scrollBanner;
     /* animations execute in sequence: */
     animation-delay           : 4s               , 5s;
     animation-duration        : 1s               , 25s;
     animation-iteration-count : 1                , infinite;
     animation-fill-mode       : backwards        , none;
     /* 'none' does not clobber previous animation: ^^^^ */
 }

==Timing functions==

...

[[Image:animDelay.png]]

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