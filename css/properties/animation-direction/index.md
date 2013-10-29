{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Defines whether an animation should run in reverse on some or all cycles.}}
{{CSS Property
|Initial value=normal
|Applies to=All elements, &#58;&#58;before and &#58;&#58;after pseudo-elements.
|Inherited=No
|Media=visual
|Computed value=As specified.
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=normal
|Description=All iterations of the animation are played as specified.
}}{{CSS Property Value
|Data Type=reverse
|Description=All iterations of the animation are played in the reverse direction from the way they were specified.
}}{{CSS Property Value
|Data Type=alternate
|Description=The animation cycle iterations that are odd counts are played in the normal direction, and the animation cycle iterations that are even counts are played in a reverse direction, thus reversing direction each cycle. The count to determine if an iteration is even or odd starts at one (odd).
}}{{CSS Property Value
|Data Type=alternate-reverse
|Description=The animation cycle iterations that are odd counts are played in the reverse direction, and the animation cycle iterations that are even counts are played in a normal direction, again reversing direction each cycle. The count to determine if an iteration is even or odd starts at one (odd).
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=A repeating pulse animation that shrinks and dims an element, then restores it. Change the '''animation-direction''' from ''normal'' to a different keyword value to see the effect.
|Code=div.selected {
    animation-name: pulse;
    animation-duration: 0.5s;
    animation-direction: alternate;
    animation-iteration-count: infinite;
}

@keyframes pulse {
    from {
        transform : scale(1) translateX(0);
        opacity : 1;
    }
    to {
        transform : scale(0.75) translateX(0);
        opacity : 0.25;
    }
}
|LiveURL=http://code.webplatform.org/gist/7010365
}}
}}
{{Notes_Section
|Usage=Can also be a comma-separated list of directions, e.g., '''reverse, normal, alternate''', where each direction is applied to the corresponding ordinal position value of the [[css/properties/animation-name|animation-name]] property.
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
|Browser=Firefox
|Version=< 15.0
|Note=Supports only normal and alternate
}}{{Compatibility Notes Row
|Browser=Opera
|Version=12.0
|Note=Supports only normal and alternate
}}{{Compatibility Notes Row
|Browser=Safari
|Version=< 6.0
|Note=Supports only normal and alternate
}}{{Compatibility Notes Row
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
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}