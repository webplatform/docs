{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Specifies how many times an animation cycle should play.}}
{{CSS Property
|Initial value=1
|Applies to=all elements
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=No
|Values={{CSS Property Value
|Data Type=single-animation-iteration-count
|Description=<code>&lt;number&gt;</code> or <code>infinite</code>.

;<code>&lt;number&gt;</code>
:The default value is <code>1</code>, which plays the animation once, from beginning to end. Numbers other than <code>1</code> cause the animation to play the specified number of times. Non-integer numbers cause the animation to end part-way through a cycle.
;<code>infinite</code>
:The animation repeats forever.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Robert Nyman introduces CSS Animations as a way to control animations, the number of times it should iterate and property values at certain keyframes.
|Code=-webkit-animation-iteration-count: infinite;
|LiveURL=[http://robertnyman.com/2010/05/06/css3-animations/ Robert Nyman's examples]
}}{{Single Example
|Language=CSS
|Description=A ''pulse'' animation that simultaneously shrinks and dims an icon. Setting the iteration-count to '''infinite''' repeats it indefinitely.
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
|Usage=This property accepts non-integer values. If a non-integer value is specified, the animation terminates mid-cycle. If <code>0</code> is specified, no animation is applied. If a negative value is specifed, the value is ignored and <code>0</code> is used instead.

Multiple values separated by commas are applied to the corresponding animations listed in the <code>animation-name</code> property. Excess values are ignored. If fewer values are listed, the browser cycles through them again until each animation has been assigned an iteration count.
|Import_Notes====Syntax===
<code>'''animation-iteration-count : '''1 '''{{!}}''' ''
&lt;number&gt;
'' '''{{!}}''' infinite '''[''' ,  1 '''{{!}}''' ''
&lt;number&gt;
'' '''{{!}}''' infinite ''']''' *</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkID{{=}}223144 CSS Animations Module Level 3], Section 3.5
}}
{{Related_Specifications_Section
|Specifications={{Related Specification}}
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