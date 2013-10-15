{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Defines an animation's direction, including whether an animation runs in reverse in some or all cycles.}}
{{CSS Property
|Initial value=normal
|Applies to=all elements
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=No
|Values={{CSS Property Value
|Data Type=normal
|Description=The animation should play forward each cycle. In other words, each time the animation cycles, the animation will reset to the beginning state and start over again. This is the default animation direction setting.
}}{{CSS Property Value
|Data Type=alternate
|Description=The animation should reverse direction each cycle. When playing in reverse, the animation steps are performed backward. In addition, timing functions are also reversed; for example, an ''<code>ease-in</code>'' animation is replaced with an ''<code>ease-out</code>'' animation when played in reverse. The count to determine if it is an even or an odd iteration starts at one.
}}{{CSS Property Value
|Data Type=reverse
|Description=The animation plays backward each cycle. Each time the animation cycles, the animation resets to the end state and start over again.
}}{{CSS Property Value
|Data Type=alternate-reverse
|Description=The animation plays backward on the first play-through, then forward on the next, then continues to alternate. The count to determine if it is an even or an odd iteration starts at one.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=animation-direction: alternate;
|LiveURL=http://03sq.net/examples/animation-direction.html
}}{{Single Example
|Language=CSS
|Description=A repeating ''pulse'' animation that simultaneously shrinks and dims an icon.
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
}}{{Single Example
|Language=CSS
|Description=The animation above progresses from one state to another, then uses '''animation-direction''' to reverse course on even-numbered iterations. The final effect appears the same as the following version, which does ''not'' alternate direction, which specifies the entire sequence from beginning to end, and which requires twice the duration to execute.
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
|Usage=The <code>animation-direction</code> property takes as its value a keyword indicating the direction of a single animation cycle. If multiple keywords are separated by commas, they are applied to each animation in the same order as specified in <code>animation-name</code>. The number of values specified for <code>animation-direction</code> doesn't need to match. If there are more values than for <code>animation-name</code>, the excess values are ignored. If there are fewer, the browser cycles through them again until each animation has been assigned a direction.
}}
{{Related_Specifications_Section
|Specifications=
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
|IE_mobile_prefixed_supported=Unknown
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}