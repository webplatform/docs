{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Defines what values are applied by the animation outside the time it is executing (before and after the animation). 

By default, an animation does not affect property values between the time it is applied (when the [[css/properties/animation-name|animation-name]] property is set on an element) and the time it begins execution (determined by the [[css/properties/animation-delay|animation-delay]] property). Also, by default an animation does not affect property values after the animation ends (determined by the [[css/properties/animation-duration|animation-duration]] property). The [[css/properties/animation-fill-mode|animation-fill-mode]] property can override this behavior. 
}}
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
|Description=Property values do not change before the animation starts, and they return to their original state when the animation ends. This is the default behavior. 
}}{{CSS Property Value
|Data Type=forwards
|Description=When the animation ends (as determined by its [[css/properties/animation-iteration-count|animation-iteration-count]]), properties retain the values set by the final keyframe. If '''animation-iteration-count''' is zero, apply the values that would start the first iteration. 

:{{{!}} class="mw-datatable os-suggest-results filehistory"
{{!}}-
! [[css/properties/animation-direction|animation-direction]]
! [[css/properties/animation-iteration-count|animation-iteration-count]]
! last keyframe encountered
{{!}}-
{{!}} <code>normal</code> 
{{!}} <code>even</code> or <code>odd</code>  
{{!}} 100% or <code>to</code> 
{{!}}-
{{!}} <code>reverse</code> 
{{!}} <code>even</code> or <code>odd</code> 
{{!}} 0% or <code>from</code> 
{{!}}-
{{!}} <code>alternate</code> 
{{!}} <code>even</code> 
{{!}} 0% or <code>from</code> 
{{!}}-
{{!}} <code>alternate</code> 
{{!}} <code>odd</code> 
{{!}} 100% or <code>to</code>
{{!}}-
{{!}} <code>alternate-reverse</code> 
{{!}} <code>even</code> 
{{!}} 100% or <code>to</code>
{{!}}-
{{!}} <code>alternate-reverse</code> 
{{!}} <code>odd</code> 
{{!}} 0% or <code>from</code>
{{!}}}

}}{{CSS Property Value
|Data Type=backwards
|Description=If the animation is delayed by [[css/properties/animation-delay|animation-delay]], properties assume values set by the first keyframe while waiting for the animation to start. These are either the values of the ''from'' keyframe (when [[css/properties/animation-direction|animation-direction]] is '''normal''' or '''alternate''') or those of the ''to'' keyframe (when [[css/properties/animation-direction|animation-direction]] is '''reverse''' or '''alternate-reverse'''). When the animation ends, properties revert to their original state.

:{{{!}} class="mw-datatable os-suggest-results filehistory"
{{!}}-
! [[css/properties/animation-direction|animation-direction]]
! first relevant keyframe
{{!}}-
{{!}} <code>normal</code> or <code>alternate</code> 
{{!}} 0% or <code>from</code>
{{!}}-
{{!}} <code>reverse</code> or <code>alternate-reverse</code> 
{{!}} 100% or <code>to</code>
{{!}}}

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
    from { transform : translateY(0em) }
    to   { transform : translateY(3em) }
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
|Manual_links=*[[tutorials/css_animations|Making things move with CSS3 animations]]
*[[css/atrules/@keyframes|@keyframes]]
*[[css/properties/animation|animation]]
*[[css/properties/animation-delay|animation-delay]]
*[[css/properties/animation-direction|animation-direction]]
*[[css/properties/animation-duration|animation-duration]]
*[[css/properties/animation-iteration-count|animation-iteration-count]]
*[[css/properties/animation-name|animation-name]]
*[[css/properties/animation-timing-function|animation-timing-function]]
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