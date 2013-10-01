{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Defines the list of animations that apply to the element}}
{{CSS Property
|Initial value=none
|Applies to=all elements, &#58;&#58;before and &#58;&#58;after pseudo-elements
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS object model property=animationName
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=none
|Description=No animation applies to the element. This is the initial value of the property.
}}{{CSS Property Value
|Data Type=<single-animation-name> [, <single-animation-name>]*
|Description=One or more comma-separated animation names. Each name is used to select the <code>[[css/atrules/@keyframes|'''@keyframes''']]</code> rule that defines the animation. If the specified name does not match any <code>[[css/atrules/@keyframes|'''@keyframes''']]</code> rule then no animation will be run for this name. In addition, when multiple animations update the same property the animation closest to the end of the list wins.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=A simple slide-in animation that executes once, much like a transition.
|Code=h1 {
  animation-duration: 3s;
  animation-name: slidein;
}
 
@keyframes slidein {
  from {
    margin-left: 100%;
    width: 300%
  }
 
  to {
    margin-left: 0%;
    width: 100%;
  }
}
|LiveURL=https://developer.mozilla.org/en-US/docs/CSS/Tutorials/Using_CSS_animations
}}{{Single Example
|Language=CSS
|Description=a repeating ''pulse'' animation that simultaneously shrinks and dims an icon
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
|LiveURL=http://letmespellitoutforyou.com/samples/anim_pulse.html
}}
}}
{{Notes_Section
|Usage=*Note that <code>animation-name</code> is not sufficient to run an animation. The <code>[[css/properties/animation-duration|animation-duration]]</code> property also needs to be set to a non-zero duration.
*When <code>animation-name</code> specifies a list of names, other animation properties such as <code>[[css/properties/animation-duration|animation-duration]]</code> should define values corresponding to each name. If the lists of values for the other animation properties do not have the same number of values as <code>animation-name</code>, the length of the <code>animation-name</code> list determines the number of items in each list examined when starting animations. The lists are matched up from the first value: excess values at the end are not used. If one of the other properties doesn't have enough comma-separated values to match the number of values of <code>animation-name</code>, the UA must calculate its used value by repeating the list of values until there are enough. This truncation or repetition does not affect the computed value. Note: This is analogous to the behavior of the background properties, with <code>[[css/properties/background-image|background-image]]</code> analogous to <code>[[css/properties/animation-name|animation-name]]</code>.
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
|Opera_version=12.10
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
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}