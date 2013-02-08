{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Sets the keyframes for the CSS [[css/properties/animation/animation|animation]] property.}}
{{CSS_At_Rule}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Example of prefixed/prefix-free @keyframes blocks
|Code=/* defining the animation */
@keyframes fadeInAnimation {
    /* starting state */
    from {
        opacity: 0;
    }
    /* ending state */
    to {
        opacity: 1;
    }
}

@-moz-keyframes fadeInAnimation {
    /* starting state */
    from {
        opacity: 0;
    }
    /* ending state */
    to {
        opacity: 1;
    }
}

@-ms-keyframes fadeInAnimation {
    /* starting state */
    from {
        opacity: 0;
    }
    /* ending state */
    to {
        opacity: 1;
    }
}

@-webkit-keyframes fadeInAnimation {
    /* starting state */
    from {
        opacity: 0;
    }
    /* ending state */
    to {
        opacity: 1;
    }
}

@-o-keyframes fadeInAnimation {
    /* starting state */
    from {
        opacity: 0;
    }
    /* ending state */
    to {
        opacity: 1;
    }
}

/* applying the animation */
div {
    animation: fadeInAnimation linear;
    -moz-animation: fadeInAnimation linear;
    -ms-animation: fadeInAnimation linear;
    -webkit-animation: fadeInAnimation linear;
    -o-animation: fadeInAnimation linear;
}
|LiveURL=http://03sq.net/examples/animation.html
}}{{Single Example
|Language=CSS
|Description=Example of an unprefixed @keyframes block that uses percentages to control the keyframes more exactly.
|Code=@keyframes bounceFadeInAnimation {
    /* starting state (same as "from") */
    0% {
        opacity: 0;
    }
    10% {
        opacity: 0.4;
    }
    15% {
        opacity: 0;
    }
    25% {
        opacity: 0.6;
    }
    50% {
        opacity: 0;
    }
    65% {
        opacity: 0.8;
    }
    80% {
        opacity: 0;
    }
    /* ending state (same as "to") */
    100% {
        opacity: 1;
    }
}
|LiveURL=http://03sq.net/examples/animation2.html
}}
}}
{{Notes_Section
|Notes====Remarks===
The version of this rule using a vendor prefix, '''@-ms-keyframes''', has been deprecated. To ensure compatibility in the future, applications using this rule with a vendor prefix should be updated accordingly.
This rule has no default value.
This rule is used to specify property values at various points during an animation. The '''@keyframes''' rule specifies the property values during one cycle of an animation; the animation may iterate one or more times.
This rule uses keyframe selectors to specify property values at various stages of the animation. Keyframe selectors can be declared as <code>from</code> (equivalent to <code>0%</code>), <code>to</code> (equivalent to <code>100%</code>), and one or more  percentages.
Keyframe selectors use keyframe descriptors to specify the properties and values being animated. If a property cannot be animated, the specification is ignored.
'''Important'''  Because of the preliminary status of the CSS Animations Module Level 3 Working Draft, the '''@keyframes''' rule must be used with the Microsoft-specific vendor prefix, "-ms-", to work with Internet Explorer 10 and Metro style apps using JavaScript.
|Import_Notes====Syntax===
<code>'''@keyframes '''''
&lt;identifier&gt;
'' { ''
&lt;keyframes_blocks&gt;
'' };</code>
===Parameters===
;''identifier'':The name of the animation.
;''keyframes_blocks'':A set of keyframes blocks, each of which is composed of keyframe selectors.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkID{{=}}223144 CSS Animations Module Level 3], Section 2
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Basic Support
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
|Opera_version=12.10
|Opera_prefixed_supported=Yes
|Opera_prefixed_version=12
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=4.0
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Yes
|Android_prefixed_version=4.0
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=Yes
|Blackberry_prefixed_version=7.0
|Chrome_mobile_supported=No
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Yes
|Chrome_mobile_prefixed_version=18.0
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Yes
|Firefox_mobile_prefixed_version=15.0
|IE_mobile_supported=Unknown
|IE_mobile_version=
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
}}{{Compatibility Table Mobile Row
|Feature=Partial Support
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Yes
|Android_prefixed_version=2.1
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=No
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=10
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=iOS Safari
|Version=all
|Note=Only some properties are hardware accelerated, this is also the case with [[css/properties/transition|transitions]]. Known properties are: opacity, translate3d. There may be more, but it is hard to find documentation for this.
}}
}}
{{See_Also_Section
|Topic_clusters=Animation, Syntax
|Manual_links=*[http://caniuse.com/#feat=css-animation canIUse Compatibility Table]
*[https://developer.mozilla.org/en-US/docs/CSS/@keyframes MDN]
|Manual_sections====Related pages (MSDN)===
*<code>[[css/properties/animation-name|animationName]]</code>
*<code>[[css/properties/animation/animation]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}