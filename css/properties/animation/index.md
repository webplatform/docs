{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Shorthand property to define a CSS animation, setting all parameters at once.}}
{{CSS Property
|Initial value=See individual properties.
|Applies to=All elements, &#58;&#58;before and &#58;&#58;after pseudo-elements.
|Inherited=No
|Media=visual
|Computed value=See individual properties.
|Animatable=No
|CSS percentages=See individual properties.
|Values={{CSS Property Value
|Data Type=single-animation [, single-animation]*
|Description=A list of values for each of the individual animation properties. The animation name and duration are required; all other values are optional. Multiple animations can be assigned as a comma-separated list.

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

'''Note:''' The first <code>&lt;time&gt;</code> value is assigned to the '''animation-duration'''. The second <code>&lt;time&gt;</code> value is assigned to the '''animation-delay'''.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=See [[css/properties/animation-play-state|animation-play-state]] for an example that uses the animation shorthand property.
|Code=nav.expanded > div.selected {
    animation: pulse 1s infinite;
}

|LiveURL=http://code.webplatform.org/gist/7044978
}}{{Single Example}}
}}
{{Notes_Section
|Usage=The <code>animation</code> shorthand property combines all animation properties except '''[[css/properties/animation-play-state|animation-play-state]]''' in a single declaration. The name and duration of the animation are required, but all other values are optional. When two <code>&lt;time&gt;</code> values are supplied, the first is assigned to the duration, and the second to the delay.

Values for a single animation are separated by spaces. Multiple animations can be assigned as a comma-separated list.
|Notes=Before the advent of CSS3, most animations were performed by using Javascript to move HTML DOM elements. This was not optimal, as the browser would not know anything about the DOM element it was moving until it executed the Javascript which moved it, making hardware accelerating animations difficult for vendors. So, CSS3's animation module was born. 

This module allows browser vendors to better support animations with hardware acceleration, especially important on CPU constrained devices such as mobile devices. Because the browser controls the  inbetween state, or ''tween'' as it is more commonly known, between two animation states, it can fully hardware accelerate the resultant animation. This leads to lower CPU usage, smoother graphics and less battery intensive web pages on mobile devices.

Animations use keyframes to specify points of animation and timing to state when those keyframes should appear. Those keyframes exist in a separate [[css/atrules/@keyframes|'''@keyframes''']] section in the CSS. The browser automatically handles the "tween" between each keyframe property. Animation is a shorthand property that defines all the properties of an animation in a single declaration. Animation applies to all elements. See the keyframes section linked above for a list of properties that can be animated.

Also, see [[tutorials/css_animations|this CSS animations tutorial]].
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Animations
|URL=http://www.w3.org/TR/css3-animations/
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
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
|Manual_links=*[[tutorials/css_animations|Making things move with CSS3 animations]]
*[[css/atrules/@keyframes|@keyframes]]
*[[css/properties/animation-delay|animation-delay]]
*[[css/properties/animation-direction|animation-direction]]
*[[css/properties/animation-duration|animation-duration]]
*[[css/properties/animation-fill-mode|animation-fill-mode]]
*[[css/properties/animation-iteration-count|animation-iteration-count]]
*[[css/properties/animation-name|animation-name]]
*[[css/properties/animation-play-state|animation-play-state]]
*[[css/properties/animation-timing-function|animation-timing-function]]

}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}