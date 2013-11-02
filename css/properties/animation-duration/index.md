{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Defines the length of time an animation takes to complete one cycle.}}
{{CSS Property
|Initial value=0s
|Applies to=All elements, &#58;&#58;before and &#58;&#58;after pseudo-elements.
|Inherited=No
|Media=visual
|Computed value=As specified.
|Animatable=No
|CSS object model property=animationDuration
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=&#60;time&#62;
|Description=Can be specified in seconds or milliseconds, e.g., '''2s''' or '''150ms'''. Can also be a comma-separated list of durations, e.g., '''.25s, .5s, 1s''', where each duration is applied to the corresponding ordinal position value of the [[css/properties/animation-name|animation-name]] property.

''The initial value of 0s means the animation takes no time; that is, it is applied instantaneously. When the duration is 0s (or 0ms), [[css/properties/animation-fill-mode|animation-fill-mode]] still applies, such that an animation filling backward will show the value of the 0% [[css/atrules/@keyframes|keyframe]] during any [[css/properties/animation-delay|delay]] period, while an animation filling forward will retain the value specified at the 100% [[css/atrules/@keyframes|keyframe]] even if the animation was instantaneous. Also, animation events are still fired.''
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=An animation duration of 5 seconds; runs once, does not repeat.
|Code=div.duration {
    animation-duration: 5s;
}
|LiveURL=http://code.webplatform.org/gist/7010824
}}{{Single Example
|Language=CSS
|Description=A repeating pulse animation that shrinks and dims an element, then restores it.
|Code=div.selected {
    animation-name: pulse;
    animation-duration: 1s;
    animation-iteration-count: infinite;
}

@keyframes pulse {
    from {
        transform : scale(1) translateX(0);
        opacity : 1;
    }
    50% {
        transform : scale(0.75) translateX(0);
        opacity : 0.25;
    }
    to {
        transform : scale(1) translateX(0);
        opacity : 1;
    }
}
|LiveURL=http://code.webplatform.org/gist/7010365
}}
}}
{{Notes_Section
|Usage=*Negative duration values are invalid and cause the entire property value to be ignored.
*If <code>[[css/properties/animation-duration|animation-duration]]</code> specifies more durations than there are values in <code>[[css/properties/animation-name|animation-name]]</code>, the excess durations are ignored.
*If <code>[[css/properties/animation-duration|animation-duration]]</code> specifies fewer durations than there are values in <code>[[css/properties/animation-name|animation-name]]</code>, the list of durations is repeated as many times as necessary to ensure each animation has a duration.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Animations
|URL=http://www.w3.org/TR/css3-animations/
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
|Manual_links=*[[tutorials/css_animations|Making things move with CSS3 animations]]
*[[css/atrules/@keyframes|@keyframes]]
*[[css/properties/animation|animation]]
*[[css/properties/animation-delay|animation-delay]]
*[[css/properties/animation-direction|animation-direction]]
*[[css/properties/animation-fill-mode|animation-fill-mode]]
*[[css/properties/animation-iteration-count|animation-iteration-count]]
*[[css/properties/animation-name|animation-name]]
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