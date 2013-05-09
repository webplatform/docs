{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Cleanup, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Sets the pace of action within a transition}}
{{CSS Property
|Initial value=ease
|Applies to=all elements
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS object model property=transitionTimingFunction
|Values={{CSS Property Value
|Data Type=ease
|Description=Default. Starts and stops gradually, equivalent to [[css/functions/cubic-bezier|'''cubic-bezier(0.25,0.1,0.25,1)''']]
}}{{CSS Property Value
|Data Type=linear
|Description=Starts and stops immediately, progressing at a constant rate, equivalent to [[css/functions/cubic-bezier|'''cubic-bezier(0,0,1,1)''']].
}}{{CSS Property Value
|Data Type=ease-in
|Description=Starts gradually and stops suddenly, equivalent to [[css/functions/cubic-bezier|'''cubic-bezier(0.42,0,1,1)''']].
}}{{CSS Property Value
|Data Type=ease-out
|Description=Starts suddenly and stops gradually, equivalent to [[css/functions/cubic-bezier|'''cubic-bezier(0,0,0.58,1)''']].
}}{{CSS Property Value
|Data Type=ease-in-out
|Description=Starts and stops gradually, equivalent to [[css/functions/cubic-bezier|'''cubic-bezier(0.42,0,0.58,1)''']].
}}{{CSS Property Value
|Data Type=[[css/functions/cubic-bezier|'''cubic-bezier()''']]
|Description=Function value specifying a customized response curve.
}}{{CSS Property Value
|Data Type=[[css/functions/steps|'''steps()''']]
|Description=Function value specifying a series of discrete intervals.
}}{{CSS Property Value
|Data Type=step-start
|Description=The change occurs instantly at the start of the keyframe, equivalent to [[css/functions/steps|'''steps(1, start)''']].
}}{{CSS Property Value
|Data Type=step-end
|Description=The change occurs instantly at the end of the keyframe, equivalent to [[css/functions/steps|'''steps(1, end)''']].
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|LiveURL=[https://developer.mozilla.org/en-US/docs/CSS/animation-timing-function] See MDN's CSS animation examples
}}
}}
{{Notes_Section
|Usage=Along with other transition properties, multiple values
separated by commas apply to transitions in the same order as they are
listed by the [[css/properties/transition-name|'''transition-name''']]
property. Excess values are ignored. If there are fewer timing values
than transitions, they're recycled in order of declaration until their
numbers match.
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