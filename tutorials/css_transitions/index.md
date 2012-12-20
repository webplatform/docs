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
traditionally used to move things around, and execute much faster.

While transitions allow you to apply all sorts of marginal
enhancements such as hover effects to traditional desktop interfaces,
they are particularly useful for small-screen mobile interfaces where
some displaying elements need to slide or fade out of view, or else
collapse into icons.  While introducing some broadly useful
techniques, the set of examples below focuses on situations where
transitions may drive key components of a mobile interface.



<!--

==The transition property==

* simple expanded/collapsed panel

* transition shorthand

* P property: all; everything that varies (vvv for what can't vary)

* P duration: 0.5s



==Expanding a panel==

[[Image:transit_simple.png]]

* 

==Timing functions==

* P timing

* curves, keywords

* steps

==Transitional sequences==

* multiple transitions

* P delay: 

* bidirectional

==The transitionend event==

* self-dismissing

* TIP: spurious transitions as alternative to setTimeout

==Cross-fades, filters, and other advanced image effects==

* default?
* cross-fade
* hue-rotate

==What can transitions control?==

* no generated ::before & ::after

* numeric
* color
* not discrete values
* gradients?
* mismatching

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