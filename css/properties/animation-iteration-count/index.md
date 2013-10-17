{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Specifies how many times an animation cycle should play.}}
{{CSS Property
|Initial value=1
|Applies to=All elements, &#58;&#58;before and &#58;&#58;after pseudo-elements.
|Inherited=No
|Media=visual
|Computed value=As specified.
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=&#60;single-animation-iteration-count&#62;
|Description=The animation plays the specified number of times. Can also be a comma-separated list of counts, e.g., '''5, 2, 10''', where each duration is applied to the corresponding ordinal position value of the [[css/properties/animation-name|animation-name]] property. Negative values are not allowed.
}}{{CSS Property Value
|Data Type=infinite
|Description=The animation repeats "forever" while the page is loaded.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=A repeating pulse animation that shrinks and dims an element, then restores it. Change the '''animation-iteration-count'' from ''infinite'' to a number to see the effect.
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
|Usage=This property accepts non-integer values, although this is not specifically mentioned in the specification; use with caution. If a non-integer value is specified, the animation terminates mid-cycle.
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
}}
}}
{{See_Also_Section
|External_links=*[http://robertnyman.com/2010/05/06/css3-animations Robert Nyman's examples]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}