{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The CSS3 Animation module describes a way for authors to animate CSS properties over time. 

Before the advent of CSS3, most animations were performed by using Javascript to move HTML DOM elements. This was not optimal, as the browser would not know anything about the DOM element it was moving until it executed the Javascript which moved it, making hardware accelerating animations difficult for vendors. So, CSS3's animation module was born. 

This module allows browser vendors to better support animations with hardware acceleration, especially important on CPU constrained devices such as mobile devices. Because the browser controls the  inbetween state, or tween as it is more commonly known, between two animation states, it can fully hardware accelerate the resultant animation. This leads to lower CPU usage, smoother graphics and less battery intensive web pages on mobile devices.

Animations use keyframes to specify points of animation and timing to state when those keyframes should appear. Those keyframes exist in a separate [[css/atrules/@keyframes|'''@keyframes''']] section in the CSS. The browser automatically handles the "tween" between each keyframe property. Animation is a shorthand property that defines all the properties of an animation in a single declaration. Animation applies to all elements. See the keyframes section linked above for a list of properties that can be animated.
Also, see [[tutorials/css_animations|this CSS animations tutorial]]
}}
{{CSS Property
|Initial value=(see individual properties)
|Applies to=all elements, :before and :after pseudo elements.
|Inherited=No
|Media=visual
|Computed value=Same as specified value.
|Animatable=No
|Values={{CSS Property Value
|Data Type=single-animation
|Description=A space-separated list of values for each of the individual animation properties. The animation name and duration are required. All other values are optional.

;<code>&lt;single-animation-name&gt;</code>
:Value of the [[css/properties/animation-name|'''animation-name''']] property.
;<code>&lt;single-animation-duration&gt;</code>
:Value of the [[css/properties/animation-duration|'''animation-duration''']] property.
;<code>&lt;single-animation-timing-function&gt;</code>
:Value of the [[css/properties/animation-timing-function|'''animation-timing-function''']] property.
;<code>&lt;single-animation-delay&gt;</code>
:Value of the [[css/properties/animation-delay|'''animation-delay''']] property.
;<code>&lt;single-animation-iteration-count&gt;</code>
:Value of the [[css/properties/animation-iteration-count|'''animation-iteration-count''']] property.
;<code>&lt;single-animation-direction&gt;</code>
:Value of the [[css/properties/animation-direction|'''animation-direction''']] property.
;<code>&lt;single-animation-fill-mode&gt;</code>
:Value of the [[css/properties/animation-fill-mode|'''animation-fill-mode''']] property.

'''Note''' The first <code>&lt;time&gt;</code> value is assigned to the '''animation-duration'''. The second <code>&lt;time&gt;</code> value is assigned to the '''animation-delay'''.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=The <code>animation</code> shorthand property combines all animation properties except <code>animation-play-state</code> in a single declaration. The name and duration of the animation are required, but all other values are optional. When two <code>&lt;time&gt;</code> values are supplied, the first is assigned to the duration, and the second to the delay.

Values for a single animation are separated by spaces. Multiple animations can be assigned as a comma-separated list.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkID{{=}}223144 CSS Animations Module Level 3], Section 3.9
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=4.0
|Firefox_supported=Yes
|Firefox_version=16.0
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=5.0
|Internet_explorer_supported=Yes
|Internet_explorer_version=10.0
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.1
|Opera_prefixed_supported=Yes
|Opera_prefixed_version=12.0
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
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=Yes
|Blackberry_prefixed_version=7.0
|Chrome_mobile_supported=No
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Yes
|Chrome_mobile_prefixed_version=18.0
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=16.0
|Firefox_mobile_prefixed_supported=Yes
|Firefox_mobile_prefixed_version=15.0
|IE_mobile_supported=Yes
|IE_mobile_version=10.0
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=12.1
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Yes
|Safari_mobile_prefixed_version=3.2
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=10.0
|Note=The -ms- prefix property is deprecated and should not be used.
}}{{Compatibility Notes Row
|Browser=Chrome
|Version=All so far
|Note=Chrome currently uses a lot of CPU resources when animations are played as the animation is hardware accelerated, however, as it moves it reports its position back to the dom many times per second. Safari doesn't seem to suffer from this problem.  This issue can be tracked here: http://code.google.com/p/chromium/issues/detail?id=130850
}}
}}
{{See_Also_Section
|Topic_clusters=Animation
|Manual_links=[[tutorials/css_animations|" the CSS animations tutorial"]]
[[css/atrules/@keyframes|'''@keyframes''']]
|Manual_sections====Related pages (W3C)===
http://www.w3.org/TR/css3-animations/
http://dev.w3.org/csswg/css3-transitions/#animatable-properties-
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[html/elements/a|a]]</code>
*<code>abbr</code>
*<code>[[html/elements/acronym|acronym]]</code>
*<code>b</code>
*<code>bdo</code>
*<code>big</code>
*<code>br</code>
*<code>cite</code>
*<code>code</code>
*<code>dfn</code>
*<code>em</code>
*<code>i</code>
*<code>img</code>
*<code>input</code>
*<code>kbd</code>
*<code>label</code>
*<code>q</code>
*<code>samp</code>
*<code>select</code>
*<code>small</code>
*<code>span</code>
*<code>strong</code>
*<code>sub</code>
*<code>sup</code>
*<code>textArea</code>
*<code>tt</code>
*<code>var</code>
*<code>address</code>
*<code>blockQuote</code>
*<code>div</code>
*<code>dl</code>
*<code>fieldSet</code>
*<code>form</code>
*<code>noFrames</code>
*<code>noScript</code>
*<code>ol</code>
*<code>p</code>
*<code>pre</code>
*<code>[[html/elements/table|table]]</code>
*<code>ul</code>
*<code>dd</code>
*<code>dt</code>
*<code>li</code>
*<code>tBody</code>
*<code>td</code>
*<code>tFoot</code>
*<code>th</code>
*<code>tHead</code>
*<code>tr</code>
*<code>button</code>
*<code>del</code>
*<code>ins</code>
*<code>map</code>
*<code>object</code>
*<code>script</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}