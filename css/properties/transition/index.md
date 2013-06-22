{{Page_Title}}
{{Flags
|Content=Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The transition CSS property is a shorthand property for [[css/properties/transition-property|transition-property]], [[css/properties/transition-duration|transition-duration]], [[css/properties/transition-timing-function|transition-timing-function]], and [[css/properties/transition-delay|transition-delay]]. It allows to define the transition between two states of an element.}}
{{CSS Property
|Initial value=see individual properties
|Applies to=all elements, :before and :after pseudo elements
|Inherited=No
|Media=interactive
|Computed value=as specified
|Animatable=No
|CSS object model property=transition
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=transition-property
|Description=Value of the [[css/properties/transition-property|'''transition-property''']] property.
}}{{CSS Property Value
|Data Type=transition-duration
|Description=Value of the [[css/properties/animation-duration|'''transition-duration''']] property.
}}{{CSS Property Value
|Data Type=transition-timing-function
|Description=Value of the [[css/properties/animation-timing-function|'''transition-timing-function''']] property.
}}{{CSS Property Value
|Data Type=transition-delay
|Description=Value of the [[css/properties/animation-delay|'''transition-delay''']] property.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=When you hover over the div, the height property will gradually change from 100 to 500.
|Code=div {
  height: 100px;
  transition: height 2s;
}

div:hover {
  height: 500px;
}
|LiveURL=http://03sq.net/examples/transition.html
}}
}}
{{Notes_Section
|Import_Notes=A list of translatable properties exists here: http://www.w3.org/TR/2009/WD-css3-transitions-20091201/#animatable-properties-
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=26
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=1
|Firefox_supported=Yes
|Firefox_version=16
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=4
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12
|Opera_prefixed_supported=Yes
|Opera_prefixed_version=11.6
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=3
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Yes
|Android_prefixed_version=2
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=Yes
|Blackberry_prefixed_version=7
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=26
|Chrome_mobile_prefixed_supported=Yes
|Chrome_mobile_prefixed_version=1
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=16
|Firefox_mobile_prefixed_supported=Yes
|Firefox_mobile_prefixed_version=4
|IE_mobile_supported=Yes
|IE_mobile_version=10
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=12.10
|Opera_mobile_prefixed_supported=Yes
|Opera_mobile_prefixed_version=10
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Yes
|Safari_mobile_prefixed_version=3.2
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Animation, Transitions
}}
{{Topics|CSS, Vendor Prefix}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/transition
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}