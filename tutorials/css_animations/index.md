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

To get the most out of this tutorial, you should already be familiar
with [[tutorials/css_transitions|CSS transitions]].  Since they work
similarly, the term ''CSS animations'' often serves as a shorthand to
refer to transitions as well, but this tutorial only discusses
''keyframe animations''.

==Animation properties==



...

<!--
    -webkit-animation: pulse 1s infinite;
* pulse == icon is selected
* name
* duration
-->

==The @keyframes rule==


...

<!--

@-webkit-keyframes pulse {
    from { 
        -webkit-transform : scale(1) translateX(0);
        opacity           : 1;
    }
    50% { 
        -webkit-transform : scale(0.75) translateX(0);
        opacity           : 0.25;
    }
    to { 
        -webkit-transform : scale(1) translateX(0);
        opacity           : 1;
    }
}

* @keyframes, @-webkit-keyframes
* EXAMPLE: pulse icon
* using from/50%/to
* using 0%/50%/100%
-->

==Direction and iteration==

...

<!--
* iteration-count
* direction
* from/to
* EXAMPLE: pulse icon using direction/iteration
-->

==Multiple animations==

...

<!--
* simultaneous for different elements
* multiple for an element
* EXAMPLE: pulse opacity and scale transform
* can't animate (or transition) the same property at the same time
* EXAMPLE: insertBanner, then cycleBanner
-->

==Fill mode==

...

<!--
* animations override style sheets
* fill-mode overrides prior to or following animation's execution
* EXAMPLE: insertBanner persists after executing
-->

==Timing functions==

...

<!--
* animation-timing-function
* same as for transitions
* can change function mid-execution
* EXAMPLE: skew transform slide-in panels
-->

==Dynamic keyframes==

...

<!--
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