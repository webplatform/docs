{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Defines the list of animations that apply to the element.}}
{{CSS Property
|Initial value=none
|Applies to=All elements, &#58;&#58;before and &#58;&#58;after pseudo-elements
|Inherited=No
|Media=visual
|Computed value=As specified.
|Animatable=No
|CSS object model property=animationName
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=none
|Description=No animation applies to the element. You can use this value to override any animations coming from the cascade.
}}{{CSS Property Value
|Data Type=<single-animation-name> [, <single-animation-name>]*
|Description=One or more comma-separated animation names. Each name is used to select the <code>[[css/atrules/@keyframes|@keyframes]]</code> rule that defines the animation. If the specified name does not match any '''@keyframes''' rule then no animation will be run for this name. In addition, when multiple animations update the same property, the animation listed last wins.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=A slide-in animation that executes once, much like a transition.
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
|LiveURL=http://code.webplatform.org/gist/7009934
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
|Usage=Note that <code>animation-name</code> is not sufficient to run an animation. The <code>[[css/properties/animation-duration|animation-duration]]</code> property also needs to be set to a non-zero duration.
When <code>animation-name</code> specifies a list of names, other animation properties such as <code>[[css/properties/animation-duration|animation-duration]]</code> should define values corresponding to each name. If the lists of values for the other animation properties do not have the same number of values as <code>animation-name</code>, the length of the <code>animation-name</code> list determines the number of items in each list examined when starting animations. The lists are matched up from the first value: excess values at the end are not used. If one of the other properties doesn't have enough comma-separated values to match the number of values of <code>animation-name</code>, the list is repeated until there are enough. This truncation or repetition does not affect the computed value. 
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
|Manual_links=*[[tutorials/css_animations{{!}}Making things move with CSS3 animations]]
*[[css/atrules/@keyframes{{!}}@keyframes]]
*[[css/properties/animation{{!}}animation]]
*[[css/properties/animation-delay{{!}}animation-delay]]
*[[css/properties/animation-direction{{!}}animation-direction]]
*[[css/properties/animation-duration{{!}}animation-duration]]
*[[css/properties/animation-fill-mode{{!}}animation-fill-mode]]
*[[css/properties/animation-iteration-count{{!}}animation-iteration-count]]
*[[css/properties/animation-timing-function{{!}}animation-timing-function]]

}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}