{{Page_Title}}
{{Flags
|High-level issues=Data Not Semantic
|Content=Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Defines the length of time an animation will take to complete one cycle}}
{{CSS Property
|Initial value=0s
|Applies to=all elements, &#58;&#58;before and &#58;&#58;after pseudo-elements
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS object model property=animationDuration
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=0s
|Description=The initial value of 0s means the animation takes no time. When the duration is 0s (or 0ms) [[css/properties/animation-fill-mode|animation-fill-mode]] still applies i.e. an animation filling backwards will show the value of the 0% [[css/atrules/@keyframes|keyframe]] during any [[css/properties/animation-delay|delay]] period, while an animation filling forwards will retain the value specified at the 100% [[css/atrules/@keyframes|keyframe]], even if the animation was instantaneous. Also, animation events are still fired.
}}{{CSS Property Value
|Data Type=1s
|Description=The specified animation will run for one second.
}}{{CSS Property Value
|Data Type=150ms
|Description=Animation duration can also be specified in milliseconds.
}}{{CSS Property Value
|Data Type=.25s, .5s
|Description=<code>animation-duration</code> can specify a comma-separated list of durations; each duration is applied to the corresponding value of <code>[[css/properties/animation-name|animation-name]]</code>.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=An animation duration of 5 seconds.
|Code=animation-duration: 5s;
|LiveURL=http://03sq.net/examples/animation-duration.html
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