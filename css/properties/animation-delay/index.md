{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Defines the length of time that must elapse before an animation starts}}
{{CSS Property
|Initial value=0s
|Applies to=all elements, &#58;&#58;before and &#58;&#58;after pseudo-elements
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS object model property=animationDelay
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=0s
|Description=The initial value of 0s means the animation will start executing as soon as it is applied through the [css/properties/animation-name|'''animation-name'''] property.
}}{{CSS Property Value
|Data Type=.25s, 100ms
|Description=This value defines the initial delay for two animations. Like durations, delays can be specified in seconds or milliseconds.
}}{{CSS Property Value
|Data Type=-1.5s
|Description=If the value for '''animation-delay''' is negative then the animation will execute the moment it is applied but will begin execution at the specified offset. That is, the animation appears to begin part-way through its play cycle.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=A delay of half a second. Example shows a delay of 5 seconds.
|Code=animation-delay: 500ms;
|LiveURL=http://03sq.net/examples/animation-delay.html
}}{{Single Example
|Language=CSS
|Description=An example of a mobile interface in which concurrent ''moveContent'' and ''insertBanner'' animations introduce a banner header after a 4-second delay. A subsequent ''scrollBanner'' animation uses a similar delay to start 5 seconds after the page loads.
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
|Usage=*If <code>[[css/properties/animation-deley|animation-delay]]</code> specifies more delays than there are values in <code>[[css/properties/animation-name|animation-name]]</code>, the excess delays are ignored.
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
|Internet_explorer_version=10
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}