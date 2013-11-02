{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Describes how the animation will progress over one cycle of its duration.}}
{{CSS Property
|Initial value=ease
|Applies to=all elements, &#58;&#58;before and &#58;&#58;after pseudo-elements
|Inherited=No
|Media=visual
|Computed value=As specified.
|Animatable=No
|CSS object model property=animationTimingFunction
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=ease
|Description=Default. The animation begins and ends gradually; this value is equivalent to <code>[[css/functions/cubic-bezier|cubic-bezier(0.25,0.1,0.25,1)]]</code>.
}}{{CSS Property Value
|Data Type=linear
|Description=The animation begins and progresses at a constant rate over the specified duration; this value is equivalent to <code>[[css/functions/cubic-bezier|cubic-bezier(0,0,1,1)]]</code>
}}{{CSS Property Value
|Data Type=ease-in
|Description=The animation begins gradually and progresses at a steady rate; this value is equivalent to <code>[[css/functions/cubic-bezier|cubic-bezier(0.42,0,1,1)]]</code>.
}}{{CSS Property Value
|Data Type=ease-out
|Description=The animation begins at a steady rate then gradually ends; this value is equivalent to <code>[[css/functions/cubic-bezier|cubic-bezier(0,0,0.58,1)]]</code>.
}}{{CSS Property Value
|Data Type=ease-in-out
|Description=The animation begins and ends gradually; equivalent to <code>[[css/functions/cubic-bezier|cubic-bezier(0.42,0,0.58,1)]]</code>. Note that this timing function is similar to <code>ease</code>, although the latter starts faster than it ends.
}}{{CSS Property Value
|Data Type=cubic-bezier(0,0,1,1)
|Description=Specifies a cubic bezier curve. The four values specify points P1 and P2 of the curve as (x1, y1, x2, y2). Both x values must be in the range [0, 1] or the definition is invalid. The y values can exceed this range. This function is used to specify custom timing functions.
}}{{CSS Property Value
|Data Type=steps(3, end)
|Description=Specifies a stepping function using two parameters. The first parameter specifies the number of intervals in the function. It must be a positive integer greater than 0. The second optional is either the value <code>start</code> or <code>end</code> and specifies the point at which the change of values occur within the interval. If the second parameter is omitted, it is given the value <code>end</code>.
}}{{CSS Property Value
|Data Type=step-start
|Description=Equivalent to steps(1,start).
}}{{CSS Property Value
|Data Type=step-end
|Description=Equivalent to steps(1,end).
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=A fast-moving sequence uses linear timing to highlight an abrupt transition within the keyframes, from a moving to a stopped state:
|Code=div {
    animation-duration        : 0.5s;
    animation-fill-mode       : both;
    animation-iteration-count : 1;
    animation-name            : fastSlide;
    animation-timing-function : linear;
    transform-origin          : bottom;
}
@keyframes fastSlide {
    0%   { transform: translate(120%) skewX(-30deg) ; }
    70%  { transform: translate(0%)   skewX(-30deg) ; }
    80%  { transform: translate(0%)   skewX(20deg)  ; }
    95%  { transform: translate(0%)   skewX(-10deg) ; }
    100% { transform: translate(0%)   skewX(0deg)   ; }
}
|LiveURL=http://code.webplatform.org/gist/7011239
}}
}}
{{Notes_Section
|Usage=The timing functions supported by <code>animation-timing-function</code> are defined by <code>[[css/properties/transition-timing-function|transition-timing-function]]</code>.

If <code>[[css/properties/animation-timing-function|animation-timing-function]]</code> specifies more timing functions than there are values in <code>[[css/properties/animation-name|animation-name]]</code>, the excess functions are ignored. If <code>[[css/properties/animation-timing-function|animation-timing-function]]</code> specifies fewer durations than there are values in <code>[[css/properties/animation-name|animation-name]]</code>, the list of functions is repeated as many times as necessary to ensure each animation has a duration.

For a keyframed animation, the '''animation-timing-function''' applies between keyframes, not over the entire animation. For example, in the case of an '''ease-in-out''' timing function, an animation will ease in at the start of the keyframe and ease out at the end of the keyframe. An '''animation-timing-function''' defined within a keyframe block applies to that keyframe, otherwise the timing function specified for the animation is used. 
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
|Note=The -ms- prefix property is deprecated and should not be used.
}}
}}
{{See_Also_Section
|Manual_links=*[[tutorials/css_animations|Making things move with CSS3 animations]]
*[[css/atrules/@keyframes|@keyframes]]
*[[css/properties/animation|animation]]
*[[css/properties/animation-delay|animation-delay]]
*[[css/properties/animation-direction|animation-direction]]
*[[css/properties/animation-duration|animation-duration]]
*[[css/properties/animation-fill-mode|animation-fill-mode]]
*[[css/properties/animation-iteration-count|animation-iteration-count]]
*[[css/properties/animation-name|animation-name]]
*[[css/properties/animation-play-state|animation-play-state]]
|External_links=* A [https://developer.mozilla.org/en-US/docs/Web/CSS/timing-function detailed description of timing functions] (MDN)
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}