{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Cleanup, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Controls the state of animated properties before and after an animation}}
{{CSS Property
|Initial value=none
|Applies to=all elements
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=No
|Values={{CSS Property Value
|Data Type=single-animation-fill-mode
|Description=One of the following values: <code>none</code> (default), <code>forwards, backwards, both</code>
 
;<code>none</code>
:Property values do not change before the animation starts, and they return to their original state when the animation ends.
;<code>forwards</code>
:When the animation ends, properties retain the values set by the final keyframe.
;<code>backwards</code>
:If the animation is delayed by <code>animation-delay</code>, properties assume values set by the first keyframe while waiting for the animation to start. When the animation ends, properties revert to their original state.
;<code>both</code>
:Values set by the first and last keyframes are applied before and after the animation.

:The animation-fill-mode property can be specified on its own, or as a property of the animation element. (See http://docs.webplatform.org/wiki/css/properties/animation/animation )
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=h1 {
  animation-fill-mode: forwards;
}
|LiveURL=[http://www.valhead.com/2013/01/04/tutorial-css-animation-fill-mode/ Val Head's examples with tutorial video]
}}{{Single Example
|Language=CSS
|Description=A more complex example of a mobile interface in which two concurrent animations displace content with a banner header. Without any animations, both elements would share the same space on the screen. In the ''moveContent'' animation, the fill mode of '''forwards''' means its end state (moved downward) persists after it finishes executing. In the ''insertBanner'' animation, the fill mode of '''backwards''' means its start state (off-screen) takes precedence over the element's CSS during the delay before the animation executes. (In the subsequent ''scrollBanner'' animation, the fill-mode is explicitly set to '''none''' to keep its initial state from
overriding that of the previous animation.)
|Code=article {
    animation-name : moveContent;
    animation-duration : 1s;
    animation-delay : 4s;
    animation-iteration-count : 1;
    animation-fill-mode : forwards;
}

header {
    animation-name : insertBanner , scrollBanner;
    animation-duration : 1s , 20s;
    animation-delay : 4s , 5s;
    animation-fill-mode : backwards , none;
    animation-iteration-count : 1 , infinite;
}

@keyframes moveContent {
    from { -webkit-transform : translateY(0em) }
    to   { -webkit-transform : translateY(3em) }
}

@keyframes insertBanner {
    from { transform : translateY(-6em) }
    to   { transform : translateY(0em) }
}


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

|LiveURL=http://letmespellitoutforyou.com/samples/anim_banner.html 
}}
}}
{{Notes_Section
|Usage=The <code>animation-fill-mode</code> property controls the state of an element's properties before and after an animation.

If multiple values are set as a comma-separated list, each value is applied to the corresponding animation specified in the <code>animation-name</code> property. If the number of values exceeds the number of animations, excess values are ignored. If there are fewer values than animations, the browser cycles through them again until each animation has been assigned a fill mode.
|Notes=This is an experimental specification, and therefore not completely finalized. Syntax and behavior are still subject to change in future versions.
|Import_Notes====Syntax===
<code>'''animation-fill-mode : '''none '''{{!}}''' forwards '''{{!}}''' backwards '''{{!}}''' both '''[''' ,  none '''{{!}}''' forwards '''{{!}}''' backwards '''{{!}}''' both ''']''' *</code>
===Standards information===
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
|Safari_prefixed_version=4.0
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
|IE_mobile_version=WP 8 (IE 10)
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
}}
}}
{{See_Also_Section
|Topic_clusters=Animation
|Manual_sections====Related pages (MSDN)===
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