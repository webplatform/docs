{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Defines what values are applied by the animation outside the time it is executing (before and after the animation).}}
{{CSS Property
|Initial value=none
|Applies to=All elements, &#58;&#58;before and &#58;&#58;after pseudo-elements.
|Inherited=No
|Media=visual
|Computed value=As specified.
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=none
|Description=Property values do not change before the animation starts, and they return to their original state when the animation ends.
}}{{CSS Property Value
|Data Type=forwards
|Description=When the animation ends, properties retain the values set by the final keyframe.
}}{{CSS Property Value
|Data Type=backwards
|Description=If the animation is delayed by <code>animation-delay</code>, properties assume values set by the first keyframe while waiting for the animation to start. When the animation ends, properties revert to their original state.
}}{{CSS Property Value
|Data Type=both
|Description=Values set by the first and last keyframes are applied before and after the animation.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=An example of a mobile-like interface in which two concurrent animations displace content with a banner header. Without any animations, both elements would overlay the same screen area. In the ''moveContent'' animation, the fill mode of '''forwards''' means its end state (moved downward) persists after it finishes executing. In the ''insertBanner'' animation, the fill mode of '''backwards''' means its start state (off-screen) takes precedence over the element's CSS during the delay before the animation executes. (In the subsequent ''scrollBanner'' animation, the fill-mode is explicitly set to '''none''' to keep its initial state from overriding that of the previous animation.)
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
|LiveURL=http://code.webplatform.org/gist/7012307
}}
}}
{{Notes_Section
|Usage=Can also be a comma-separated list of fill modes, e.g., '''forwards, none, backwards''', where each fill mode is applied to the corresponding ordinal position value of the [[css/properties/animation-name|animation-name]] property.
|Notes=This is an experimental specification, and therefore not completely finalized. Syntax and behavior are still subject to change in future versions.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Animation
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
}}
}}
{{See_Also_Section
|External_links=* See also [http://www.valhead.com/2013/01/04/tutorial-css-animation-fill-mode/ Val Head's examples with tutorial video].
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}