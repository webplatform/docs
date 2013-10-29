{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Defines a length of time to elapse before an animation starts, allowing an animation to begin execution some time after it is applied.}}
{{CSS Property
|Initial value=0s
|Applies to=All elements, &#58;&#58;before and &#58;&#58;after pseudo-elements
|Inherited=No
|Media=visual
|Computed value=As specified.
|Animatable=No
|CSS object model property=animationDelay
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=&#60;time&#62;
|Description=Can be specified in seconds or milliseconds, e.g., '''2s''' or '''150ms'''. Can also be a comma-separated list of delays, e.g., '''.25s, .5s, 1s''', where each delay is applied to the corresponding ordinal position value of the [[css/properties/animation-name|animation-name]] property.

''If the value is negative the animation will execute the moment it is applied, but will begin execution at the specified offset. That is, the animation appears to begin part-way through its cycle.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=A delay of 5 seconds.
|Code=div.animationDelay {
    animation-delay: 5s;
}
|LiveURL=http://code.webplatform.org/gist/7011569
}}{{Single Example
|Language=CSS
|Description=An example of a mobile-like interface in which concurrent ''moveContent'' and ''insertBanner'' animations introduce a colored banner header after a 4-second delay. A subsequent ''scrollBanner'' animation uses a similar delay to start 5 seconds after the page loads.
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
|Usage=*If <code>[[css/properties/animation-delay|animation-delay]]</code> specifies more delays than there are values in <code>[[css/properties/animation-name|animation-name]]</code>, the excess delays are ignored.
*If <code>[[css/properties/animation-delay|animation-delay]]</code> specifies fewer delays than there are values in <code>[[css/properties/animation-name|animation-name]]</code>, the list of delays is repeated as many times as needed to map each animation to a delay.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Animations
|URL=http://www.w3.org/TR/css3-animations/#animation-delay-property
|Status=Working Draft
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
|Note=The -ms- prefixed property is deprecated and should not be used.
}}
}}
{{See_Also_Section
|Topic_clusters=Animation
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/animation-delay
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}